# Structure du MDN (MSSanté) - Volet Transmission au LPS de documents CDA provenant d'un courriel MSSanté v1.1.3

* [**Table of Contents**](toc.md)
* **Structure du MDN (MSSanté)**

## Structure du MDN (MSSanté)

Le MDN (Message Disposition Notification), défini par la [RFC 8098](https://datatracker.ietf.org/doc/html/rfc8098), permet de notifier l’émetteur d’un courriel du traitement de ce courriel par son destinataire. Il est produit conformément à cette RFC, qui en fixe la structure et les conditions d’émission ([§2.1](https://datatracker.ietf.org/doc/html/rfc8098#section-2.1)) : en particulier, un MDN ne peut être émis que si le courriel reçu porte un entête `Disposition-Notification-To`.

>  La [RFC 8098](https://datatracker.ietf.org/doc/html/rfc8098) demeure la référence pour la structure du MDN ; le présent volet se limite à préciser les informations que le MDN doit véhiculer pour permettre son traitement automatisé. 

### Éligibilité au mécanisme MDN

Pour MSSanté, le MDN est prescrit par le [Référentiel socle MSSanté #2](https://esante.gouv.fr/espace_documentation/mssante-clients-de-messageries-securisees-de-sante/referentiel-socle-mssante-2), qui en délègue la structure à la [RFC 8098](https://datatracker.ietf.org/doc/html/rfc8098) sans en définir d’autre :

* `ECO.2.3.2` : le client émetteur doit pouvoir demander un accusé de lecture ;
* `ECO.3.1.6` : le client destinataire doit retourner un MDN lorsque le message reçu le demande.

Ce référentiel s’applique aux logiciels métier des professionnels habilités, pour des échanges manuels comme automatisés, mais « ne s’applique donc pas aux interfaces webmail ou clients de messageries standards (type Outlook ou Thunderbird) ».

Le référentiel précise l’usage attendu du mécanisme : il « permet de savoir que le message a bien été reçu par le destinataire et quel traitement il a effectué lors de la réception du message : lecture, intégration des pièces jointes dans le système cible ». L’emploi que le présent volet en fait — rendre compte de l’intégration du document dans le DPI — relève donc de ce que le socle prévoit.

### Objet du MDN

Dans le cas d’un MDN en erreur, l’objet du MDN doit être précisé de la façon suivante : `[KO Intégration système !][code erreur] XDM/1.0/DDM+<libellé> <NOM> <prénom> <date de naissance>`.

Dans le cas contraire, l’objet du MDN est précisé par `XDM/1.0/DDM+<libellé> <NOM> <prénom> <date de naissance>`.

### Structure du corps du MDN

Le MDN est de type `multipart/report` ([RFC 6522](https://datatracker.ietf.org/doc/html/rfc6522#section-3)) : `Content-Type: multipart/report; report-type=disposition-notification; boundary="<frontière>"`

Dans le contexte du présent volet, il comporte les trois parties suivantes :

| | | |
| :--- | :--- | :--- |
| 1 | `text/plain` | Texte lisible par un être humain |
| 2 | `message/disposition-notification` | Compte rendu exploitable par une machine |
| 3 | `message/rfc822` | Courriel d’origine : ses entêtes, son corps et ses pièces jointes |

Ces trois parties répondent à trois besoins distincts : la première permet à un utilisateur de comprendre ce qui s’est passé, la deuxième permet à la PFI réceptrice de traiter la notification sans intervention humaine, et la troisième lui restitue le courriel d’origine, sans lequel elle ne pourrait ni identifier le document concerné ni le soumettre à nouveau après correction.

>  **Point d'attention :** un MDN ne s'affiche pas de la même façon selon le client de messagerie qui le reçoit. Le texte de la première partie est affiché par la plupart des clients. En revanche, la deuxième et la troisième partie peuvent être présentées comme des fichiers joints, voire masquées, et le courriel d'origine peut n'être proposé qu'au téléchargement, sous la forme d'un fichier `.eml`. Une personne chargée de reprendre l'erreur peut donc ne voir d'emblée que la première partie, et devoir ouvrir le courriel d'origine pour accéder aux documents. C'est pourquoi la première partie doit au moins contenir le code et le libellé de l'erreur. Ce point mérite d'être vérifié à l'intégration. 

#### Première partie : texte lisible par un être humain

Cette partie contient du texte lisible par un être humain. Dans le contexte du présent volet, ce texte doit au moins contenir, en cas d’erreur, le code et le libellé de l’erreur retournés par le CONSOMMATEUR.

* Par exemple : « `Le message ci-dessous n’a pas pu être intégré automatiquement dans le DPI pour la raison suivante : <code erreur> <libellé de l’erreur>` ».

#### Deuxième partie : compte rendu exploitable par une machine

Cette partie, de type `message/disposition-notification`, est construite conformément à la [RFC 8098 §3](https://datatracker.ietf.org/doc/html/rfc8098#section-3). Dans le contexte du présent volet, ses champs sont renseignés comme suit :

* Le champ « `Disposition:` » ([RFC 8098 §3.2.6](https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.6)) rend compte du résultat du traitement du courriel :
* Le champ « `Error:` » ([RFC 8098 §3.2.7](https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.7)) est obligatoire en cas d’erreur. Il reprend la chaîne d’erreur retournée par le CONSOMMATEUR dans le segment `ERR` de son accusé de réception, qui porte au minimum `code erreur^libellé erreur`.
* Le champ « `Original-Message-ID:` » ([RFC 8098 §3.2.5](https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.5)) est obligatoire : il permet à la PFI réceptrice de rapprocher le MDN du courriel d’origine.
* Les champs « `Final-Recipient:` » et « `Original-Recipient:` » sont renseignés selon le tableau ci-dessous.
* Le champ « `Reporting-UA:` » ([RFC 8098 §3.2.1](https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.1)) identifie la PFI qui a produit le MDN.

##### Valeurs attendues des champs d’adressage

Le tableau ci-dessous précise les valeurs attendues dans le contexte MSSanté décrit par le présent volet : le courriel est réceptionné sur une BAL organisationnelle, puis transféré vers la BAL applicative associée, et le MDN est produit par la PFI pour le compte de cette BAL applicative.

| | | |
| :--- | :--- | :--- |
| `From:`du MDN | La BAL applicative qui a réceptionné le courriel traité, et pour le compte de laquelle le MDN est produit |   |
| `To:`du MDN | L’adresse indiquée dans l’entête`Disposition-Notification-To`du courriel traité — dans le cas d’usage décrit par ce volet, la BAL organisationnelle du service destinataire | [RFC 8098 §3](https://datatracker.ietf.org/doc/html/rfc8098#section-3) |
| `Original-Recipient:` | Lorsque ce champ est présent : l’adresse du destinataire telle que spécifiée par l’expéditeur du courriel traité, soit la BAL applicative | [RFC 8098 §3.2.3](https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.3) |
| `Final-Recipient:` | L’adresse du destinataire pour lequel le MDN est émis, soit la BAL applicative | [RFC 8098 §3.2.4](https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.4) |

#### Troisième partie : courriel d’origine

Cette partie contient le courriel d’origine restitué **dans son intégralité** : ses entêtes, son corps et ses pièces jointes. **Aucun élément ne doit être perdu.**

En cas d’erreur, l’objectif est que le destinataire du MDN dispose de tous les éléments nécessaires au retraitement sans avoir à retrouver le courriel d’origine par un autre moyen : identifier le document et l’usager concernés, corriger ce qui a fait échouer l’intégration, et soumettre à nouveau les documents. Le courriel d’origine étant restitué comme objet, il reste réinjectable tel quel dans une chaîne de traitement.

Les pièces jointes envoyées avec le courriel d’origine (IHE_XDM.zip et le pdf) sont restituées au sein de cette partie, puisqu’elle porte le courriel d’origine complet. Il n’est pas nécessaire de les reprendre en outre comme pièces jointes du MDN : cela doublerait le volume du message sans apporter d’information supplémentaire, et placerait ces copies dans des parties dont la RFC 6522 ne spécifie pas le traitement.

Cet emplacement ne contrevient pas au [Référentiel socle MSSanté #2](https://esante.gouv.fr/espace_documentation/mssante-clients-de-messageries-securisees-de-sante/referentiel-socle-mssante-2) : son exigence `ECO.2.1.1` — un courriel transmettant des documents de santé doit contenir « en pièces jointes du courriel » une archive `IHE_XDM.zip` et les mêmes documents médicaux au format PDF/A-1 — porte sur le courriel MSSanté qui transmet les documents, et non sur la notification qui en rend compte. La troisième partie restituant ce courriel tel quel, ses pièces jointes demeurent à l’emplacement que le référentiel prescrit.

Le socle veut par ailleurs que le destinataire d’un courriel transmettant des documents de santé puisse en prendre connaissance « sans avoir besoin d’un LPS (cas d’un webmail ou d’une application mobile) grâce au(x) fichier(s) PDF ». La restitution intégrale du courriel d’origine préserve cette possibilité : le PDF y figure tel qu’il a été transmis, et le destinataire du MDN y accède en ouvrant le courriel encapsulé.

### Exemple d’un MDN

L’exemple suivant décrit le MDN (accusé de lecture négatif) généré dans le contexte du cas d’usage [Transmission d’un document clinique d’un patient d’un établissement hospitalier vers un autre établissement hospitalier](volume1.md#description-du-cas-dusage-en-erreur) du présent volet.

Il est fourni à titre **illustratif et n’a pas valeur normative** : les exigences du volet sont portées par les paragraphes qui précèdent. Les valeurs qu’il contient (adresses, identifiants, dates, frontières MIME) sont fictives.

Le nom du fichier PDF suit la convention de nommage `ECO.2.1.6` du [Référentiel socle MSSanté #2](https://esante.gouv.fr/espace_documentation/mssante-clients-de-messageries-securisees-de-sante/referentiel-socle-mssante-2), dont le caractère `_` sépare les champs et dont les libellés admettent espaces et caractères accentués.

Les entêtes d’un courriel ne peuvent porter que des caractères US-ASCII ([RFC 5322](https://datatracker.ietf.org/doc/html/rfc5322)) : dans un courriel réel, l’entête `Subject:` doit être encodé selon la [RFC 2047](https://datatracker.ietf.org/doc/html/rfc2047) et les paramètres `name` et `filename` selon la [RFC 2231](https://datatracker.ietf.org/doc/html/rfc2231). Ces formes ne sont pas reprises dans l’exemple, pour en préserver la lisibilité. Pour ce fichier, la forme conforme du paramètre serait `filename*=UTF-8''20220531_CR%20d%27imagerie%20m%C3%A9dicale_CORSE_FIGATELLIX.pdf`.

```
Date: Tue, 20 Feb 2024 00:19:00 +0100 (CET)
From: serviceY_auto@chb.mssante.fr
Message-ID: <20240220001900.12345@chb.mssante.fr>
Subject: [KO Intégration système !][902] XDM/1.0/DDM+ECHOGRAPHIE ABDOMINOPELVIENNE CORSE FIGATELLIX 12/10/1988
To: serviceY@chb.mssante.fr
MIME-Version: 1.0
Content-Type: multipart/report; report-type=disposition-notification;
 boundary="RAA14128.773615765"

--RAA14128.773615765
Content-Type: text/plain; charset="UTF-8"
Content-Transfer-Encoding: 8bit

Le document n’a pas pu être intégré.
Le système a retourné l'erreur 902^Identifiant patient inconnu^applicationErrorCondition| E^Error^errorSeverity

--RAA14128.773615765
Content-Type: message/disposition-notification

Reporting-UA: pfi.chb.mssante.fr; PFI etablissement-B
Original-Recipient: rfc822;serviceY_auto@chb.mssante.fr
Final-Recipient: rfc822;serviceY_auto@chb.mssante.fr
Original-Message-ID: <20240219230100.23456@chb.mssante.fr>
Disposition: automatic-action/MDN-sent-automatically; processed/error
Error: 902^Identifiant patient inconnu^applicationErrorCondition| E^Error^errorSeverity

--RAA14128.773615765
Content-Type: message/rfc822
Content-Transfer-Encoding: 8bit

Return-Path: <serviceY@chb.mssante.fr>
Original-Recipient: rfc822;serviceY_auto@chb.mssante.fr
Date: Mon, 19 Feb 2024 23:01:00 +0100 (CET)
From: serviceY@chb.mssante.fr
To: serviceY_auto@chb.mssante.fr
Message-ID: <20240219230100.23456@chb.mssante.fr>
Subject: XDM/1.0/DDM+ECHOGRAPHIE ABDOMINOPELVIENNE CORSE FIGATELLIX 12/10/1988
Disposition-Notification-To: serviceY@chb.mssante.fr
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

