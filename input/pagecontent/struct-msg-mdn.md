La RFC 8098 définit le type de contenu
« message/disposition-notification » propre au message MDN (Message
Disposition Notification). Ce message MDN est utilisé pour notifier
l'émetteur d'un courriel de tout traitement qui survient après la
livraison de ce courriel au niveau du récepteur. Conformément à la RFC
8098, ce message MDN doit :

-   Être lisible par un humain et par une machine,

-   Fournir suffisamment d'informations pour permettre à l'émetteur du
    message d'associer sans ambiguïté le message MDN au message
    initialement envoyé et à l'adresse du récepteur initial au nom
    duquel le message MDN a été produit,

-   Être structuré conformément à la RFC 2822 et la RFC 8098,

L'envoi du message MDN à l'expéditeur du courriel initial est
conditionné par la présence d'un entête Disposition-Notification-To au
niveau du courriel expédié. D'autres informations peuvent également être
fournies en utilisant les entêtes Original-Recipient et
Disposition-Notification-Options.

La RFC 8098 précise qu'un MDN ne devrait pas être renvoyé
automatiquement par le récepteur du courriel dans le cas où l'entête
Disposition-Notification-To diffère de l'adresse précisée dans l'entête
returm-Path du courriel envoyé, ceci afin d'éviter une transmission de
messages en boucle. Dans ce cas l'envoi du MDN nécessite une
confirmation de l'utilisateur.

Dans le cas d'un MDN en erreur, l'objet du message MDN doit être précisé
de la façon suivante : \[KO Intégration système ! \]
XDM/1.0/DDM+\<libellé\> \<NOM\> \<prénom\> \<date de naissance\>.

Dans le cas contraire, l'objet du message MDN est précisé par
XDM/1.0/DDM+\<libellé\> \<NOM\> \<prénom\> \<date de naissance\>.

Le message MDN est de type « multipart/report » :
`Content-Type:multipart/report;report-type=disposition-notification; boundary="RAA14128.773615765/example.com"`

-   La première partie contient du texte lisible par un être humain.
    Dans le contexte du présent volet, ce texte doit au moins contenir,
    en cas d'erreur, le code et le libellé de l'erreur retournés par le
    CONSOMMATEUR.

    -   Par exemple : « `Le message ci-dessous n'a pas pu être intégré automatiquement dans le DPI pour la raison suivante : <libellé de l'erreur>` ».

-   La seconde partie est conforme au type de contenu message/disposition-notification constitué de différents champs d'entête formatés selon la RFC 2822. Parmi ces champs, « `Disposition:` » et `« Final-Recipient: » ` sont obligatoires :

    -   Le champ `« Disposition: »` rend compte du résultat du traitement du courriel par le destinataire^(Note\ 1)^~ :~

        -   En cas de succès, le contenu du champ « `Disposition:` » prend la valeur : « `Disposition: automatic-action/MDN-sent-automatically; processed` »

-   En cas d'erreur, le contenu du champ « Disposition: » prend la valeur : « `Disposition:automatic-action/MDN-sent-automatically; processed/Error: code erreur\^libellé erreur` »
-   Le champ « `Final-Recipient:` » qui correspond à l'adresse du destinataire pour lequel le MDN est émis. La valeur de ce champ peut être différente de l'adresse initialement fournie par l'émetteur du courriel, notamment en cas de transfert du courriel initial par le destinataire.

Dans le contexte de ce volet, de façon à permettre le traitement du message MDN par la PFI réceptrice, le message MDN devra également préciser les champs suivants :

-   Le champ identifiant du courriel d'origine « `Original-Message-ID` » qui indique l'identifiant du courriel initial pour lequel le message MDN est produit. Il est obtenu à partir de l'entête Message-ID du courriel initial.

-   Le champ « `Original-Recipient:` » qui indique l'adresse du destinataire du courriel d'origine, telle que spécifiée par l'expéditeur du courriel pour lequel le MDN est émis. Cette valeur est obtenue à partir de l'entête Original-Recipient du courriel pour lequel le message MDN est généré.
-   La troisième partie contient le corps du courriel d'origine.

Les pièces jointes envoyées avec le courriel d'origine (IHE_XDM.zip et le pdf) doivent être remises en pièces jointes du courriel MDN.

**(Note 1)** : Détail du champ obligatoire « `Disposition:` » : ce champ
permet de préciser :

-   Le mode de traitement effectué sur le courriel : traitement automatique ou manuel

    -   action-mode = \"manual-action\" / \"automatic-action\".

        -   La valeur « manual-action » indique que le traitement du courriel résulte d'une action explicite réalisée par l'utilisateur.

        -   La valeur « automatic-action » indique que le traitement du courriel a été réalisée de façon automatique.

-   Le mode d'envoi du message MDN

    -   sending mode=\"MDN-sent-manually\" / \"MDN-sent-automatically\".

        -   La Valeur "MDN-sent-manually » est utilisée lorsque l'utilisateur a donné son autorisation explicite d'envoyer un MDN particulier.

        -   La valeur MDN-sent-automatically » permet de configurer l'envoi automatique des MDN.

-   Le type de traitement réalisé

    -   disposition-type=\"displayed\" / \"deleted\" / \"dispatched\" /\"processed\"

        -   displayed : le courriel a été affiché dans la BAL du destinataire

        -   dispatched : le courriel a été dispatché (transféré, imprimé, faxé) sans que celui-ci ait nécessairement été affiché au destinataire.

        -   processed : le message a été traité sans être affiché au destinataire. Il est possible qu'il n'y ait pas d'utilisateur associé à la BAL.

        -   deleted : le courriel a été supprimé. Le destinataire peut ne pas avoir visualiser le message ou peut l'avoir visualisé.

-   Le cas échéant, l'erreur rencontrée

    -   disposition-modifier = \"error\"

Exemple d'un message MDN :

L'exemple suivant décrit le message MDN (accusé de lecture négatif) généré dans le contexte du cas d'usage « Transfert d'un patient d'un CH vers un autre CH -Gestion des erreurs » présenté au [paragraphe suivant](cas-usage.html#description-du-cas-en-erreur) du présent volet.

```
Date: Wed, 20 Feb 2024 00:19:00 (EDT) -0400
From: serviceY_auto@chb.mssante.fr
Message-Id: <199509200019.12345>
Subject: [Erreur d’intégration !] XDM/1.0/DDM+ECHOGRAPHIE ABDOMINOPELVIENNE CORSE FIGATELLIX 12/10/1988
To: serviceY@chb.mssante.fr
MIME-Version: 1.0
Content-Type: multipart/report; report-type=disposition-notification; boundary="RAA14128.773615765"
--RAA14128.773615765
Le document n’a pas pu être intégré.
Le système a retourné l'erreur 902^Identifiant de patient inconnu^messageErrorCondition| E^Error^errorSeverity
--RAA14128.773615765
Content-Type: message/disposition-notification
Original-Recipient: rfc822;serviceY_auto@chb.mssante.fr 
Final-Recipient: rfc822; serviceY_auto@chb.mssante.fr 
Original-Message-ID: <199509192301.23456 >
Disposition:automatic-action/MDN-sent-automatically; processed/Error: 902^Identifiant de patient inconnu^messageErrorCondition| E^Error^errorSeverity
--RAA14128.773615765
Content-Type: message/rfc822
Ici apparaît le contenu du courriel MSSanté à l’origine du MDN et ses pièces jointes.
--RAA14128.773615765—
Content-Type: application/zip ; name="IHE_XDM.zip"
Content-Transfert-Encoding: base64
Content-Disposition: attachment;filename= "IHE_XDM.zip"

Ici apparaît le fichier IHE_XDM.zip encode en base64.
--RAA14128.773615765—
Content-Type: application/pdf ; name="20220531_CR d'imagerie médicale_CORSE_FIGATELLIX.pdf"
Content-Transfert-Encoding: base64
Content-Disposition: attachment;filename= "20220531_CR d'imagerie médicale_CORSE_FIGATELLIX.pdf"

Ici apparaît le fichier 20220531_CR d'imagerie médicale_CORSE_FIGATELLIX.pdf encodé en base64.
--RAA14128.773615765--

```