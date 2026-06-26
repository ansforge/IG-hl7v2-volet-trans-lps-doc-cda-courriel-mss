# Codes erreurs de traitement du message HL7 MDM - Volet Transmission au LPS de documents CDA provenant d'un courriel MSSanté v1.1.3

* [**Table of Contents**](toc.md)
* **Codes erreurs de traitement du message HL7 MDM**

## Codes erreurs de traitement du message HL7 MDM

La table HL7 messageErrorCondition est utilisée par l’acteur CONSOMMATEUR (DPI/RIS…) en cas d’erreur technique du message HL7 MDM.

La nature de l’erreur est renseignée dans le champ ERR-3 de la structure du message ACK renvoyé par le CONSOMMATEUR au niveau du GESTIONNAIRE (PFI).

* Code: 0
  * Libellé: Message accepted
  * Description: Message accepté
* Code: 100
  * Libellé: Segment sequence error
  * Description: Les segments ne sont pas dans le bon ordre ou il manque un ou plusieurs segments requis
* Code: 101
  * Libellé: Required field missing
  * Description: Un champ requis dans un segment est manquant
* Code: 102
  * Libellé: Data type error
  * Description: Erreur sur un type de donnée
* Code: 103
  * Libellé: Table value not found
  * Description: Table non trouvée
* Code: 198
  * Libellé: Non-conformant cardinality
  * Description: Erreur de cardinalité sur un champ du message
* Code: 199
  * Libellé: Other HL7 Error
  * Description: Autre type d'erreur concernant la syntaxe du message HL7
* Code: 200
  * Libellé: Unsupported message type
  * Description: Type de message non supporté
* Code: 201
  * Libellé: Unsupported event code
  * Description: Code évènement non supporté
* Code: 202
  * Libellé: Unsupported processing
  * Description: Code process non supporté
* Code: 203
  * Libellé: Unsupported version
  * Description: Version HL7 non supportée
* Code: 207
  * Libellé: Application error
  * Description: Erreur de niveau applicatif dont le contenu est détaillé dans le champ ERR-5

La table user-defined applicationErrorCondition est utilisée par l’acteur CONSOMMATEUR (DPI/RIS…) en cas d’erreur d’intégration/de remplacement ou de suppression du document CDA au niveau du CONSOMMATEUR. La nature de l’erreur applicative est renseignée dans le champ ERR-5 de la structure du message ACK renvoyé par le CONSOMMATEUR au niveau du GESTIONNAIRE.

Cette table est décrite à titre indicatif et pourra être enrichie si besoin, en fonction des retours d’implémentation.

* Code: 900
  * Libellé: Version du document incorrecte lors d'une demande de remplacement/suppression
  * Description: Lors d'une demande de remplacement ou suppression d'un document, la version de document transmise dans le message HL7 ne correspond pas à la version la plus récente du document existant au niveau de l'application réceptrice (consommateur)
* Code: 901
  * Libellé: Auteur non autorisé à remplacer ou supprimer un document
  * Description: Lors d'une demande de remplacement ou suppression d'un document, l'acteur qui demande le traitement sur le document doit être l'auteur du document ou un acteur qui appartient à la même organisation que l'auteur du document original. Dans le cas contraire, le message est rejeté.
* Code: 902
  * Libellé: Identifiant patient inconnu
  * Description: Le patient pour lequel le traitement sur le document est demandé est inconnu de l'application réceptrice (consommateur)
* Code: 903
  * Libellé: INS non présent dans le document
  * Description: Le document CDA contenu dans le message contient une liste d'identifiants de patient mais pas l'INS. Dans ce cas, la demande de traitement sur le document (intégration/remplacement/suppression) ne peut pas être réalisée de façon automatique par le système consommateur.
* Code: 904
  * Libellé: L'INS transmis ne correspond pas exactement à celui stocké dans la base du consommateur
  * Description: L'INS du patient est présent dans le document CDA contenu dans le message HL7 mais les traits ou le matricule ne correspondent pas exactement à ceux stockés dans le système consommateur. Dans ce cas, la demande de traitement sur le document (intégration/remplacement/suppression) ne peut pas être réalisée de façon automatique par le système consommateur.
* Code: 905
  * Libellé: L'INS transmis n'est pas complet
  * Description: Le matricule INS du patient est présent dans le document CDA contenu dans le message HL7 mais l'ensemble des traits de l’INS ne sont pas présents. Dans ce cas, la demande de traitement sur le document (intégration/remplacement/suppression) ne peut pas être réalisée de façon automatique par le système consommateur.
* Code: 906
  * Libellé: Erreur 'Autre'
  * Description: Si les autres codes erreurs ne correspondent pas au cas d'erreur rencontré ce code erreur peut être utilisé.

