### Contexte

Si un MDN (Message Disposition Notification) n'a pas été explicitement demandé par le destinataire (via l'entête `Disposition-Notification-To` dans le message d'origine), vous ne pouvez pas utiliser un MDN tel que défini par la [RFC 8098](https://datatracker.ietf.org/doc/html/rfc8098), car il suppose qu'un accusé de réception ou une notification d'état a été requis.

Dans ce cas, pour retourner une notification similaire à celle d’un MDN, vous pouvez utiliser un courriel "standard" avec une structure et un contenu adaptés.
Ce courriel doit être compréhensible par l'humain et inclure toutes les informations nécessaires pour expliquer le problème ou fournir un retour en cas d'erreur comme pour les cas d'usage :

* [Réception d’un compte rendu de biologie par un établissement hospitalier](volume1.html#description-du-cas-en-erreur)
* [Transmission d’un document clinique d’un patient d’un établissement hospitalier vers un autre établissement hospitalier](volume1.html#description-du-cas-dusage-en-erreur)

### Contenu clé du courriel

Voici les points essentiels pour construire le courriel standard en tant que notification :

* Sujet clair : Expliquez qu'il s'agit d'une notification (ex. : "Notification de traitement du message").
* Corps du message :
  * Fournissez une explication lisible par l'humain.
  * Mentionnez le problème détecté (erreur, statut ou autre).
  * Indiquez des instructions pour corriger ou prévenir le problème.
* Inclusion du message d'origine :
Ajoutez le message d'origine (ou une partie) comme pièce jointe (`message/rfc822`).
Cela permet au destinataire de comprendre le contexte.
* Pièces jointes :
  * Les pièces jointes envoyées avec le courriel d'origine (IHE_XDM.zip et le pdf) doivent être remises en pièces jointes du courriel pour pouvoir traiter les erreurs.
  * Le contenu est encodé en Base64 pour respecter le standard MIME.

### Format du courriel

Le courriel doit respecter la [RFC 5322 'Internet Message Format'](https://datatracker.ietf.org/doc/html/rfc5322)


### Exemple de courriel

Exemple d'un courriel standard qui pourrait être envoyé comme notification manuelle. Le contenu est réorganisé pour être compréhensible par un humain, tout en respectant les principes des courriels standards avec des pièces jointes.
Cet exemple illustre le cas d'usage [Transmission d’un document clinique d’un patient d’un établissement hospitalier vers un autre établissement hospitalier](volume1.html#description-du-cas-dusage-en-erreur)


```
Date: Wed, 20 Feb 2024 00:19:00 -0400
From: serviceY_auto@chb.mssante.fr
To: serviceY@chb.mssante.fr
Message-ID: <199509200019.12345@chb.mssante.fr>
Subject: Notification : Erreur d’intégration du document "ECHOGRAPHIE ABDOMINOPELVIENNE CORSE FIGATELLIX"
MIME-Version: 1.0
Content-Type: multipart/mixed; boundary="boundary12345"

--boundary12345
Content-Type: text/plain; charset="UTF-8"
Content-Transfer-Encoding: 7bit

Bonjour,

Le document envoyé n’a pas pu être intégré correctement dans le système. 
Voici les détails de l’erreur rencontrée :

- **Erreur détectée :** Identifiant de patient inconnu
- **Code d’erreur :** 902
- **Gravité :** E (Error)

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

<Insérer ici le contenu du courriel MSSanté à l’origine du MDN et ses pièces jointes>

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
* dans le corps du message
* ou en pièce jointe, pour conserver un format structuré qui pourrait être traité par un système.

