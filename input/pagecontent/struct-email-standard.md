### Contexte

Dans le cas où un MDN (Message Disposition Notification) n'a pas été explicitement demandé par le destinataire (via l'entête `Disposition-Notification-To` dans le message d'origine), il n'est pas possible d'envoyer un  MDN tel que défini par la [RFC 8098](https://datatracker.ietf.org/doc/html/rfc8098), car il suppose qu'un accusé de réception ou une notification d'état a été requis.

Le MDN ne peut pas être utilisé pour rediriger et traiter l'ensemble des erreurs.
Dans ce cas, pour retourner une notification similaire à celle d’un MDN, il faut  utiliser un courriel "standard" avec une structure et un contenu adaptés.

Ce courriel doit 
- Être compréhensible par l'humain
- Inclure toutes les informations nécessaires pour expliquer le problème afin de le traiter
- Être structuré conformément à la RFC 2822 

### Contenu  du courriel

Le courriel standart doit être composé de la façon suivante : 

* Objet du message : il doit être précisé
de la façon suivante afin de faciliter la lecture et le traitement de la notification : `[KO Intégration système !][code erreur] XDM/1.0/DDM+<libellé> <NOM> <prénom> <date de naissance>`.
* Corps du message :
  * La première partie contient du texte lisible par un être humain. Dans le contexte du présent volet, ce texte doit au moins contenir, en cas d’erreur, le code et le libellé de l’erreur retournés par le CONSOMMATEUR.
  Par exemple : « Le message ci-dessous n’a pas pu être intégré automatiquement dans le DPI pour la raison suivante : <libellé de l’erreur> ».
* Inclusion du message d'origine : contient le corps du courriel d’origine.
* Pièces jointes :
  * Les pièces jointes envoyées avec le courriel d’origine (IHE_XDM.ZIP et le pdf) doivent être remises en pièces jointes du courriel.
  * Le contenu est encodé en Base64 pour respecter le standard MIME.

### Format du courriel

Le courriel doit respecter la [RFC 5322 'Internet Message Format'](https://datatracker.ietf.org/doc/html/rfc5322)


### Exemple de courriel

Exemple d'un courriel standard qui pourrait être envoyé comme notification manuelle. Le contenu est réorganisé pour être compréhensible par un humain, tout en respectant les principes des courriels standards avec des pièces jointes.
Cet exemple illustre le cas d'usage [Transmission d'un document clinique d'un patient d'un établissement hospitalier vers un autre établissement hospitalier](volume1.html#description-du-cas-dusage-en-erreur)


```
Date: Wed, 20 Feb 2024 00:19:00 -0400
From: serviceY_auto@chb.mssante.fr
To: serviceY@chb.mssante.fr
Message-ID: <199509200019.12345@chb.mssante.fr>
Subject: [Erreur d’intégration !][902] XDM/1.0/DDM+ECHOGRAPHIE ABDOMINOPELVIENNE CORSE FIGATELLIX 12/10/1988
MIME-Version: 1.0
Content-Type: multipart/mixed; boundary="boundary12345"

--boundary12345
Content-Type: text/plain; charset="UTF-8"
Content-Transfer-Encoding: 7bit

Bonjour,

Le document envoyé n’a pas pu être intégré correctement dans le système. 
Voici les détails de l’erreur rencontrée :

- Erreur détectée : Identifiant de patient inconnu
- Code d’erreur : 902


Vous trouverez en pièce jointe :
1. Le message original contenant le document soumis.
2. Les fichiers liés (archive ZIP et PDF associés au message original).

Veuillez vérifier les informations fournies et soumettre à nouveau les documents après correction. 
Si le problème persiste, contactez notre service technique.

Cordialement,  
L’équipe technique du service Y  

--boundary12345
Content-Type: message/rfc822
Content-Disposition: attachment; filename="message_original.eml"

<Insérer ici le contenu du courriel MSSanté à l’origine  et ses pièces jointes>

--boundary12345
Content-Type: application/zip; name="IHE_XDM.zip"
Content-Transfer-Encoding: base64
Content-Disposition: attachment; filename="IHE_XDM.zip"

<Ici apparaît le fichier IHE_XDM.zip encodé en base64>

--boundary12345
Content-Type: application/pdf; name="20220531_CR_d_imagerie_medicale_CORSE_FIGATELLIX.pdf"
Content-Transfer-Encoding: base64
Content-Disposition: attachment; filename="20220531_CR_d_imagerie_medicale_CORSE_FIGATELLIX.pdf"

<Ici apparaît le fichier 20220531_CR_d_imagerie_medicale_CORSE_FIGATELLIX.pdf encodé en base64>

--boundary12345--
```

### Différences clés avec un MDN
Contrairement à un MDN :

  Ce courriel standard est non-automatisé et non structuré pour un traitement machine. L'entête `Disposition` avec le format `processed/Error: ...` est spécifique aux MDN et n'est pas standard dans un courriel classique.
  
  Le code erreur ne peut être véhiculé que :

* Dans l'objet du message
* Dans le corps du message
* ou en pièce jointe, pour conserver un format structuré qui pourrait être traité par un système.
