La [RFC 8098](https://datatracker.ietf.org/doc/html/rfc8098) définit le type de contenu
« message/disposition-notification » propre au MDN (Message
Disposition Notification). Ce MDN est utilisé pour notifier
l'émetteur d'un courriel de tout traitement qui survient après la
livraison de ce courriel au niveau du récepteur. Conformément à la [RFC
8098](https://datatracker.ietf.org/doc/html/rfc8098), ce MDN doit :

-   Être lisible par un humain et par une machine,

-   Fournir suffisamment d'informations pour permettre à l'émetteur du
    message d'associer sans ambiguïté le MDN au message
    initialement envoyé et à l'adresse du récepteur initial au nom
    duquel le MDN a été produit,

-   Être structuré conformément à la [RFC 5322](https://datatracker.ietf.org/doc/html/rfc5322) (qui rend obsolète la RFC 2822) et la [RFC 8098](https://datatracker.ietf.org/doc/html/rfc8098),

L'envoi du MDN à l'expéditeur du courriel initial est
conditionné par la présence d'un entête Disposition-Notification-To au
niveau du courriel expédié. D'autres informations peuvent également être
fournies en utilisant les entêtes Original-Recipient et
Disposition-Notification-Options.

La [RFC 8098](https://datatracker.ietf.org/doc/html/rfc8098) précise qu'un MDN ne devrait pas être renvoyé
automatiquement par le récepteur du courriel dans le cas où l'entête
Disposition-Notification-To diffère de l'adresse précisée dans l'entête
Return-Path du courriel envoyé, ceci afin d'éviter une transmission de
messages en boucle. Dans ce cas l'envoi du MDN nécessite une
confirmation de l'utilisateur.

### Éligibilité au mécanisme MDN

Le [Référentiel socle MSSanté #2](https://esante.gouv.fr/sites/default/files/media/document/ans_mss_ref2_clients_de_messageries_mssante_v1.0.1_20240118.pdf) (v1.0.1 du 18/01/2024) rend le mécanisme MDN obligatoire dans les deux sens :

| Exigence | Énoncé |
|---|---|
| `ECO.2.3.2` | « Le système DOIT permettre de demander au destinataire un accusé de lecture (MDN) lors de l'émission d'un courriel. » |
| `ECO.3.1.6` | « Le système DOIT permettre de retourner un accusé de lecture (MDN) lorsqu'un message reçu le demande. » |

Ces exigences ne s'imposent toutefois qu'aux **clients de messagerie MSSanté**, c'est-à-dire, au sens de ce référentiel, à tout logiciel métier (client lourd ou SaaS) utilisé par un professionnel habilité et comportant des fonctions d'échange par messagerie MSSanté — que ces échanges soient réalisés manuellement au travers d'une IHM ou de façon automatisée (DPI, SIL, RIS…). Le référentiel précise qu'il « ne s'applique donc pas aux interfaces webmail ou clients de messageries standards (type Outlook ou Thunderbird) ».

<blockquote class="stu-note">
    <p>
    <b>Point d'attention :</b> la production d'un MDN n'est donc pas garantie sur l'ensemble de la chaîne. Dans le cas d'usage décrit par ce volet, le courriel parvient à la BAL applicative après un transfert depuis la BAL organisationnelle du service destinataire. Si ce transfert est réalisé au moyen d'un webmail ou d'un client de messagerie standard — hors du périmètre du Référentiel socle MSSanté #2 — rien ne garantit que l'entête <code>Disposition-Notification-To</code> soit positionné sur le courriel transféré. Or, sans cet entête, aucun MDN ne peut être émis en retour.
    <br><br>
    C'est la situation pour laquelle le volet prévoit un <a href="struct-email-standard.html">courriel standard de notification</a> en substitution du MDN.
    </p>
</blockquote>

Le Référentiel socle MSSanté #2 précise par ailleurs que, « dans la présente version du référentiel, seule l'information sur la "lecture" du message est demandée en retour, mais l'intégration des PJ dans le système cible pourrait être confirmée par le même mécanisme ». L'usage du MDN décrit dans la présente annexe — rendre compte du résultat de l'intégration du document dans le système cible — relève de cette extension que le référentiel anticipe. C'est ce qui justifie le recours au type de traitement `processed` plutôt qu'à `displayed` _(Note 1)_.

### Objet du MDN

Dans le cas d'un MDN en erreur, l'objet du MDN doit être précisé
de la façon suivante : `[KO Intégration système !][code erreur] XDM/1.0/DDM+<libellé> <NOM> <prénom> <date de naissance>`.

Dans le cas contraire, l'objet du MDN est précisé par `XDM/1.0/DDM+<libellé> <NOM> <prénom> <date de naissance>`.

### Structure du corps du MDN

Le MDN est de type « multipart/report » :

`Content-Type: multipart/report; report-type=disposition-notification; boundary="RAA14128.773615765"`

**Besoin fonctionnel :** en cas d'erreur, le MDN doit restituer au destinataire l'intégralité du courriel d'origine — entêtes, corps et pièces jointes — afin de lui permettre de traiter l'erreur (reprise manuelle, correction puis réémission).

Conformément à la [RFC 6522 §4](https://datatracker.ietf.org/doc/html/rfc6522#section-4) et à la [RFC 8098 §3](https://datatracker.ietf.org/doc/html/rfc8098#section-3), le corps d'un « multipart/report » comporte deux ou trois parties, à rôles fixés et dans un ordre imposé. Dans le contexte du présent volet, les trois parties sont attendues :

| # | `Content-Type` | Rôle | Cardinalité dans ce volet |
|---|---|---|---|
| 1 | `text/plain` | Texte lisible par un être humain | Obligatoire |
| 2 | `message/disposition-notification` | Compte rendu exploitable par une machine | Obligatoire |
| 3 | `message/rfc822` | Courriel d'origine restitué intégralement, pièces jointes comprises | Obligatoire |

Chaque partie est introduite par le délimiteur `--<boundary>` ; la dernière partie est suivie du délimiteur de clôture `--<boundary>--`, encadré de deux tirets ASCII (caractère `-`, U+002D) de part et d'autre ([RFC 2046 §5.1.1](https://datatracker.ietf.org/doc/html/rfc2046#section-5.1.1)). Au sein de chaque partie, les entêtes sont séparés du contenu par une **ligne vide** ([RFC 2045](https://datatracker.ietf.org/doc/html/rfc2045)).

#### Première partie : texte lisible par un être humain

-   Dans le contexte du présent volet, ce texte doit au moins contenir,
    en cas d'erreur, le code et le libellé de l'erreur retournés par le
    CONSOMMATEUR.

    -   Par exemple : « `Le message ci-dessous n’a pas pu être intégré automatiquement dans le DPI pour la raison suivante : <libellé de l’erreur>` ».

-   Cette partie déclare son jeu de caractères (`Content-Type: text/plain; charset="UTF-8"`), les libellés d'erreur pouvant comporter des caractères accentués.

#### Deuxième partie : compte rendu exploitable par une machine

Cette partie est conforme au type de contenu `message/disposition-notification`. Son contenu est constitué de différents champs formatés selon la [RFC 5322](https://datatracker.ietf.org/doc/html/rfc5322) et séparés de l'entête `Content-Type` de la partie par une ligne vide. Parmi ces champs, « `Disposition:` » et « `Final-Recipient:` » sont obligatoires :

-   Le champ « `Disposition:` » rend compte du résultat du traitement du courriel par le destinataire _(Note 1)_ :

    -   En cas de succès, le contenu du champ « `Disposition:` » prend la valeur : « `Disposition: automatic-action/MDN-sent-automatically; processed` »

    -   En cas d'erreur, le contenu du champ « `Disposition:` » prend la valeur : « `Disposition: automatic-action/MDN-sent-automatically; processed/Error: code erreur^libellé erreur` »

-   Le champ « `Error:` » ([RFC 8098 §3.2.7](https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.7)) est l'emplacement que la RFC 8098 prévoit pour porter un texte de diagnostic lorsque le modificateur `error` est présent. Il est recommandé d'y reprendre le code et le libellé de l'erreur, sous la forme `code erreur^libellé erreur` (voir le point d'attention ci-dessous).

-   Le champ « `Final-Recipient:` » qui correspond à l'adresse du destinataire pour lequel le MDN est émis. La valeur de ce champ peut être différente de l'adresse initialement fournie par l'émetteur du courriel, notamment en cas de transfert du courriel initial par le destinataire.

Dans le contexte de ce volet, de façon à permettre le traitement du MDN par la PFI réceptrice, le MDN devra également préciser les champs suivants :

-   Le champ identifiant du courriel d'origine « `Original-Message-ID:` » qui indique l'identifiant du courriel initial pour lequel le MDN est produit. Il est obtenu à partir de l'entête `Message-ID` du courriel initial.

-   Le champ « `Original-Recipient:` » qui indique l'adresse du destinataire du courriel d'origine, telle que spécifiée par l'expéditeur du courriel pour lequel le MDN est émis. Cette valeur est obtenue à partir de l'entête `Original-Recipient` du courriel pour lequel le MDN est généré.

Le champ « `Reporting-UA:` », qui identifie l'agent ayant produit le MDN, est recommandé par la [RFC 8098 §3.2.1](https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.1).

<blockquote class="stu-note">
    <p>
    <b>Point d'attention :</b> la valeur « <code>processed/Error: code erreur^libellé erreur</code> » du champ <code>Disposition:</code> n'est pas conforme à la grammaire de la <a href="https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.6">RFC 8098 §3.2.6</a> : un <code>disposition-modifier</code> y est défini comme un <code>Atom</code> au sens de la <a href="https://datatracker.ietf.org/doc/html/rfc5322#section-3.2.3">RFC 5322 §3.2.3</a>, lequel n'admet ni le caractère « : » ni les espaces. Le code erreur porté par cette valeur n'est donc pas exploitable par un outillage MDN standard, qui ne retiendra que « <code>processed</code> ».
    <br><br>
    Cette forme, historiquement retenue par le volet, est conservée. Le champ <code>Error:</code> permet aux CONSOMMATEURS s'appuyant sur un outillage MDN standard d'accéder à la même information.
    <br><br>
    La <a href="https://datatracker.ietf.org/doc/html/rfc8098">RFC 8098</a> demeure la référence pour la structure du MDN ; le présent volet se limite à préciser les informations que le MDN doit véhiculer pour permettre son traitement automatisé par la PFI réceptrice.
    </p>
</blockquote>

##### Valeurs attendues des champs d'adressage

Le tableau ci-dessous précise les valeurs attendues dans le contexte MSSanté décrit par le présent volet : le courriel est réceptionné sur une BAL organisationnelle puis transféré vers la BAL applicative associée, et le MDN est produit par la PFI pour le compte de cette BAL applicative.

| Champ | Valeur attendue | Référence |
|---|---|---|
| `From:` du MDN | BAL applicative qui a réceptionné le courriel traité et pour le compte de laquelle le MDN est produit | |
| `To:` du MDN | Adresse indiquée dans l'entête `Disposition-Notification-To` du courriel traité — dans le cas d'usage décrit par ce volet, la BAL organisationnelle du service destinataire | [RFC 8098 §3](https://datatracker.ietf.org/doc/html/rfc8098#section-3) |
| `Original-Recipient:` | Adresse du destinataire telle que spécifiée par l'expéditeur du courriel traité, reprise de l'entête `Original-Recipient` de ce courriel — soit la BAL applicative | [RFC 8098 §3.2.3](https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.3) |
| `Final-Recipient:` | Adresse de la BAL pour laquelle le MDN est émis. Cette valeur est **identique à celle du champ `From:`** du MDN | [RFC 8098 §3.2.4](https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.4) |

Dans le cas d'usage décrit par ce volet, le courriel traité par la PFI est celui qui a été transféré sur la BAL applicative : les champs `Original-Recipient:` et `Final-Recipient:` portent donc la même adresse, celle de la BAL applicative. Ces deux valeurs peuvent différer dans d'autres organisations, notamment lorsque le courriel est de nouveau transféré par le destinataire.

#### Troisième partie : courriel d'origine

Cette partie, de type `message/rfc822`, contient le courriel d'origine restitué **dans son intégralité** : ses entêtes, son corps et ses pièces jointes (`IHE_XDM.zip` et le pdf), encodées en base64 comme dans le courriel initial.

------------------------------------------
 **(Note 1)** : Détail du champ obligatoire « `Disposition:` » : ce champ permet de préciser :
 -   Le mode de traitement effectué sur le courriel : traitement automatique ou manuel
    -   `action-mode = "manual-action" / "automatic-action"`.

        -   La valeur « manual-action » indique que le traitement du courriel résulte d'une action explicite réalisée par l'utilisateur.

        -   La valeur « automatic-action » indique que le traitement du courriel a été réalisé de façon automatique.

-   Le mode d'envoi du MDN

    -   `sending-mode = "MDN-sent-manually" / "MDN-sent-automatically"`.

        -   La valeur « MDN-sent-manually » est utilisée lorsque l'utilisateur a donné son autorisation explicite d'envoyer un MDN particulier.

        -   La valeur « MDN-sent-automatically » permet de configurer l'envoi automatique des MDN.

-   Le type de traitement réalisé

    -   `disposition-type = "displayed" / "deleted" / "dispatched" / "processed"`

        -   displayed : le courriel a été affiché dans la BAL du destinataire

        -   dispatched : le courriel a été dispatché (transféré, imprimé, faxé) sans que celui-ci ait nécessairement été affiché au destinataire.

        -   processed : le message a été traité sans être affiché au destinataire. Il est possible qu'il n'y ait pas d'utilisateur associé à la BAL.

        -   deleted : le courriel a été supprimé. Le destinataire peut ne pas avoir visualisé le message ou peut l'avoir visualisé.

-   Le cas échéant, l'erreur rencontrée

    -   `disposition-modifier = "error"`

------------------------------------------

### Exemple d'un MDN

L'exemple suivant décrit le MDN (accusé de lecture négatif) généré dans le contexte du cas d'usage « Transmission d'un document clinique d'un patient d'un CH vers un autre CH - Gestion des erreurs » présenté au [paragraphe suivant](volume1.html#description-du-cas-dusage-en-erreur) du présent volet.

Cet exemple est fourni à titre **illustratif et n'a pas valeur normative** : les exigences du volet sont portées par les paragraphes qui précèdent. Les valeurs qu'il contient (adresses, identifiants, dates, frontières MIME) sont fictives.

Le courriel traité par la PFI de l'établissement-B est celui qui a été transféré depuis la BAL organisationnelle du service Y (`serviceY@chb.mssante.fr`) vers la BAL applicative associée (`serviceY_auto@chb.mssante.fr`). Ce courriel est restitué intégralement, pièces jointes comprises, dans la troisième partie du MDN.

```
Date: Tue, 20 Feb 2024 00:19:00 +0100 (CET)
From: serviceY_auto@chb.mssante.fr
To: serviceY@chb.mssante.fr
Message-Id: <20240220001900.12345@chb.mssante.fr>
Subject: [KO Intégration système !][902] XDM/1.0/DDM+ECHOGRAPHIE ABDOMINOPELVIENNE CORSE FIGATELLIX 12/10/1988
MIME-Version: 1.0
Content-Type: multipart/report; report-type=disposition-notification;
 boundary="RAA14128.773615765"

--RAA14128.773615765
Content-Type: text/plain; charset="UTF-8"
Content-Transfer-Encoding: 8bit

Le document n'a pas pu être intégré.
Le système a retourné l'erreur 902 : Identifiant de patient inconnu

--RAA14128.773615765
Content-Type: message/disposition-notification

Reporting-UA: pfi.chb.mssante.fr; PFI de l'établissement-B
Original-Recipient: rfc822;serviceY_auto@chb.mssante.fr
Final-Recipient: rfc822;serviceY_auto@chb.mssante.fr
Original-Message-ID: <20240219230100.23456@chb.mssante.fr>
Disposition: automatic-action/MDN-sent-automatically; processed/Error: 902^Identifiant de patient inconnu
Error: 902^Identifiant de patient inconnu

--RAA14128.773615765
Content-Type: message/rfc822

Date: Mon, 19 Feb 2024 23:01:00 +0100 (CET)
From: serviceY@chb.mssante.fr
To: serviceY_auto@chb.mssante.fr
Message-ID: <20240219230100.23456@chb.mssante.fr>
Subject: XDM/1.0/DDM+ECHOGRAPHIE ABDOMINOPELVIENNE CORSE FIGATELLIX 12/10/1988
Disposition-Notification-To: serviceY@chb.mssante.fr
Original-Recipient: rfc822;serviceY_auto@chb.mssante.fr
MIME-Version: 1.0
Content-Type: multipart/mixed; boundary="ZZZ09876.543210987"

--ZZZ09876.543210987
Content-Type: text/plain; charset="UTF-8"
Content-Transfer-Encoding: 8bit

Ici apparaît le corps du courriel MSSanté à l'origine du MDN.

--ZZZ09876.543210987
Content-Type: application/zip; name="IHE_XDM.zip"
Content-Transfer-Encoding: base64
Content-Disposition: attachment; filename="IHE_XDM.zip"

Ici apparaît le fichier IHE_XDM.zip encodé en base64.

--ZZZ09876.543210987
Content-Type: application/pdf; name="20220531_CR d'imagerie médicale_CORSE_FIGATELLIX.pdf"
Content-Transfer-Encoding: base64
Content-Disposition: attachment; filename="20220531_CR d'imagerie médicale_CORSE_FIGATELLIX.pdf"

Ici apparaît le fichier 20220531_CR d'imagerie médicale_CORSE_FIGATELLIX.pdf encodé en base64.

--ZZZ09876.543210987--

--RAA14128.773615765--
```
