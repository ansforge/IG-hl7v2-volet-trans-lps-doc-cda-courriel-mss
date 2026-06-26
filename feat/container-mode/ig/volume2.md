# Volume 2 : Détail des transactions - Volet Transmission au LPS de documents CDA provenant d'un courriel MSSanté v1.1.3

* [**Table of Contents**](toc.md)
* **Volume 2 : Détail des transactions**

## Volume 2 : Détail des transactions

### Introduction

Cette section décrit les détails techniques nécessaires à la mise en œuvre de la transaction permettant la transmission d’une demande de traitement (transmission initiale/remplacement/suppression) d’un document clinique au format CDA-R2 (Clinical Document Architecture Release 2) entre une Plateforme d’Intermédiation (PFI) et le logiciel métier du professionnel de santé, après détection d’un courriel reçu sur une Boîte Aux Lettres (BAL) MSSanté de l’établissement.

### Périmetre de la transaction

Le périmètre des spécifications s’applique à toute demande de transmission initiale/remplacement/suppression d’un document CDA-R2, provenant d’un courriel MSSanté réceptionné dans une BAL applicative et traité par la PFI de l’établissement hospitalier, accompagnée des informations du courriel et des métadonnées MSSanté associées au document. Ces informations sont encodées dans un flux HL7v2.6 MDM.

Les spécifications couvrent également l’accusé de réception du message HL7 MDM.

L’accusé de réception du message HL7 MDM rend compte de la bonne ou mauvaise intégration du message et des informations portées par le message au niveau de l’acteur CONSOMMATEUR.

### Rôle des acteurs pour cette transaction

* **Acteur**: **Rôle**
  * GESTIONNAIRE: - Le GESTIONNAIRE extrait les informations de l'archive IHE_XDM (pièce jointe du mail), analyse ces informations et construit le message HL7 MDM correspondant pour l'envoyer au CONSOMMATEUR.- Le GESTIONNAIRE réceptionne l'accusé de réception et d'intégration du message HL7 MDM, gère cet accusé et construit un accusé de lecture MSSanté (MDN-Message Disposition Notification) en fonction du statut retourné par l'acquittement du message HL7 MDM.
* **Acteur**: **Acteur**
  * GESTIONNAIRE: CONSOMMATEUR
* **Acteur**: **Rôle**
  * GESTIONNAIRE: - Le CONSOMMATEUR reçoit la demande du GESTIONNAIRE (transmission initiale/remplacement/suppression d'un document) sous la forme d'un message HL7 MDM, intègre si possible dans sa base de données les informations portées par le message HL7 MDM et renvoie vers le GESTIONNAIRE l'accusé de réception du message HL7 MDM.

### Choix des standards

* HL7 v2.6 : Chapitre 9, message MDM (Medical Document Management) (1),
* [Extension française du profil IHE PAM : PAM.fr, version 2.11](https://www.interopsante.org/publications)
* Les types de données utilisés (2) doivent se conformer aux spécifications [« Contraintes sur les types de données HL7 v2.5 applicables aux profils d’intégration du cadre technique IT Infrastructure dans le périmètre d’IHE France » release 1.8](https://www.interopsante.org/publications)
* Le choix du protocole de transport est libre. L’utilisation du protocole MLLP est à privilégier pour gérer au mieux les accusés de réception techniques (ACK).
* Dans le cadre de cette spécification, les documents médicaux véhiculés correspondent à des documents au format CDA-R2 conformes au [volet du CI-SIS « Structuration minimale des documents de santé »](https://esante.gouv.fr/volet-structuration-minimale-de-documents-de-sante).
* Les documents transmis par le message HL7 doivent être validés par le professionnel de santé dans l’application métier qui les a générés via un statut de validation géré en interne.

>  **(1) :** Les messages décrits au niveau de cette transaction implémentent la version 2.6 (message MDM) du standard HL7 mais pré adoptent le segment PRT de la version 2.9, permettant de spécifier l’expéditeur et le(s) destinataire(s) d’un courriel. Le message MDM permet de transmettre un seul document. 

>  **(2) :** Pour l'ensemble des champs de type CE en HL7v2.5 et CWE en HL7v2.6, la contrainte imposée en version 2.7 sur le type de donnée CE/CWE est pré adoptée. En conséquence, ces spécifications imposent de préciser le système de codage (CE/CWE.3) lorsque le code (CE/CWE.1) est renseigné. Les bonnes pratiques consistent à renseigner systématiquement les 3 composantes : le code, le libellé du code et le libellé de la nomenclature. 

### Evènements déclenchants

Après réception d’un courriel détecté dans une BAL applicative MSSanté, la PFI ouvre l’archive IHE_XDM contenant des documents médicaux et les transmets individuellement au LPS consommateur en utilisant un message HL7v2.6 de type MDM.

Ensuite, le LPS accuse réception de cette demande de traitement sur le document avec un message HL7v2.6 de type ACK.

* Flux métiers: TransmissionDocuments
  * Type de message HL7v2.6: Transmission initiale d'un document : L'évènement utilisé sera le T02 « Original document notification »-> `MDM^T02^MDM_T02`-> OBX-11 = F (Final results; Can only be changed with a corrected result.) [HL7 Tables 0085]
* Flux métiers: Suppression d'un document : L'évènement utilisé sera le T04 « Document status change notification and content »-> `MDM^T04^MDM_T02`-> OBX-11 = D (Deletes the OBX record) [HL7 Tables 0085]
* Flux métiers: Remplacement d'un document : L'évènement utilisé sera le T10 « Document replacement notification and content »-> `MDM^T10^MDM_T02`-> OBX-11 = C (Record coming over is a correction and thus replaces a final result) [HL7 Tables 0085]
* Flux métiers: ReponseTransmissionDocuments
  * Type de message HL7v2.6: ACK : Acquittement du message HL7 MDM

### Interactions entre les Acteurs

**Figure 13 : Diagramme de séquence – Message MDM**

 La gestion de l’accusé de lecture MSSanté (MDN-Message Disposition Notification) va dépendre de l’organisation choisie par l’établissement pour traiter les courriels réceptionnés.

Ce flux d’accusé de lecture MSSanté (courriel MDN) rend compte de la lecture du courriel par le destinataire lorsque ce courriel est traité de façon manuelle. Dans le cas d’un traitement automatique du courriel par la PFI de l’établissement destinataire, ce flux d’accusé de lecture rend compte de la réalisation de la demande de traitement sur le document contenu dans le courriel par le logiciel métier associé à la BAL destinatrice du courriel.

Dans le cas où le courriel entrant, réceptionné par une BAL organisationnelle, est transféré vers la BAL applicative associée pour traitement automatique de la demande, le courriel MDN généré par le GESTIONNAIRE (PFI) et envoyé à la BAL organisationnelle demandeuse est indispensable pour avertir l’utilisateur du succès ou de l’échec de la demande de traitement par le CONSOMMATEUR.

La structure du MDN (Message Disposition Notification) est précisée [ici](struct-msg-mdn.md).

### Profils de messages

#### Le message MDM en HL7 v2.6

##### Description du profil du message MDM

Le profil du message MDM est le suivant :

* Segment: MSH
  * Meaning: Message Header
  * Usage: R
  * Card.: [1..1]
  * § HL7: 2
* Segment:  [{SFT}]
  * Meaning: Software Segment
  * Usage: O
  * Card.: [0..*]
  * § HL7: 2
* Segment: [UAC]
  * Meaning: User Authentication Credentials
  * Usage: O
  * Card.: [0..1]
  * § HL7: 2
* Segment: EVN
  * Meaning: Event type
  * Usage: R
  * Card.: [1..1]
  * § HL7: 2
* Segment: PID
  * Meaning: Patient Identification
  * Usage: R
  * Card.: [1..1]
  * § HL7: 3
* Segment: PV1
  * Meaning: Patient Visit
  * Usage: R
  * Card.: [1..1]
  * § HL7: 3
* Segment:  
  * Meaning: --- COMMON_ORDER begin
  * Usage: R
  * Card.: [1..1]
  * § HL7:  
* Segment:  ORC
  * Meaning: Common Order = demande de service sur le document
  * Usage: R
  * Card.: [1..1]
  * § HL7: 4
* Segment:  [{
  * Meaning: --- TIMING begin
  * Usage: O
  * Card.: [0..*]
  * § HL7:  
* Segment:  TQ1
  * Meaning: Timing/Quantity
  * Usage: R
  * Card.: [1..1]
  * § HL7: 4
* Segment:  [{TQ2}]
  * Meaning: Timing/Quantity RelationShip
  * Usage: O
  * Card.: [0..*]
  * § HL7: 4
* Segment:  }]
  * Meaning: --- TIMING end
  * Usage:  
  * Card.:  
  * § HL7:  
* Segment:  OBR
  * Meaning: Observation Request segment
  * Usage: R
  * Card.: [1..1]
  * § HL7: 4
* Segment:  [{NTE}]
  * Meaning: Notes and comments
  * Usage: O
  * Card.: [0..*]
  * § HL7: 2
* Segment:  
  * Meaning: --- COMMON_ORDER end
  * Usage:  
  * Card.:  
  * § HL7:  
* Segment: TXA
  * Meaning: Transcription document header
  * Usage: R
  * Card.: [1..1]
  * § HL7: 9
* Segment: {
  * Meaning: OBXNTE (Document, informations sur le courriel, métadonnées sur le document)
  * Usage: R
  * Card.: [1..*]
  * § HL7:  
* Segment:  OBX
  * Meaning: Observation/Result
  * Usage: R
  * Card.: [1..1]
  * § HL7: 9
* Segment:  [{PRT}]
  * Meaning: Participation : Expéditeur, destinataire(s) MSS et adresse mail sur laquelle le destinataire peut répondre. Segment PRT pré-adopté de la version 2.9
  * Usage: R
  * Card.: [1..*]
  * § HL7: 7 (v2.9)
* Segment:  [{NTE}]
  * Meaning: Notes and comments
  * Usage: O
  * Card.: [0..*]
  * § HL7: 2
* Segment: }
  * Meaning: ---OBXNTE end
  * Usage:  
  * Card.:  
  * § HL7:  

Le message HL7 MDM ne peut transmettre qu’un seul document médical.

Les contraintes apportées par ce volet sur les données du message MDM sont décrites à la [section dédiée](volume2.md#contraintes-appliquées-aux-messages-mdm-dans-le-contexte-de-ce-volet).

##### Description fonctionnelle du message MDM

**Figure 14 : Description fonctionnelle du message HL7 MDM**

 Les groupes de segments en rouge sur le schéma représentent les éléments spécifiques à ce volet :

* Un groupe OBXNTE, requis, contenant le document médical au format CDA-R2 codé en base64 suivi de segments PRT, pré-adoptés depuis la version 2.9 du standard, permettant ainsi de renseigner les informations de l’expéditeur (requis), le destinataire MSSanté (requis si connu) et, le cas échéant, l’adresse mail de réponse (contraintes décrites au [paragraphe dédié](volume2.md#le-groupe-de-segments-obxnte-portant-le-document-cda)).
* Le deuxième groupe véhicule, dans un segment OBX, les informations du courriel MSSanté dont a été extrait le document.
* Les groupes OBXNTE suivants (requis et répétables) véhiculent les métadonnées spécifiques à l’envoi par la MSSanté.

Dans le message MDM, le document est accompagné de quelques métadonnées renseignées au niveau du segment TXA. Il s’agit à minima du type de document (TXA-2), de la présentation du contenu du document (TXA-3), de l’identifiant unique du document (TXA-12), de l’identifiant unique du document remplacé (TXA-13) lorsque l’évènement est à T10 et du statut indiquant la complétude du document (TXA-17).

#### Contraintes appliquées aux messages MDM dans le contexte de ce volet

Dans la suite de cette section, les valeurs indiquées en bleu dans les tableaux indiquent les valeurs fixes à insérer dans le champ du message.

##### Eléments de contrôle du message MDM

###### Le segment MSH – Header du message

* Champ: MSH-1
  * Contenu: | séparateur de champ
  * Type donnée: ST
  * Caractère optionnel/obligatoire: R
* Champ: MSH-2
  * Contenu: ^~\& : séparateur de composant, répétition, caractère d'échappement, séparateur de sous-composants
  * Type donnée: ST
  * Caractère optionnel/obligatoire: R
* Champ: MSH-3
  * Contenu: Application émettrice
  * Type donnée: HD
  * Caractère optionnel/obligatoire: R
* Champ: MSH-4
  * Contenu: Organisation émettrice
  * Type donnée: HD
  * Caractère optionnel/obligatoire: R
* Champ: MSH-5
  * Contenu: Application réceptrice
  * Type donnée: HD
  * Caractère optionnel/obligatoire: R
* Champ: MSH-6
  * Contenu: Organisation réceptrice
  * Type donnée: HD
  * Caractère optionnel/obligatoire: R
* Champ: MSH-7
  * Contenu: Date/time du message
  * Type donnée: TS
  * Caractère optionnel/obligatoire: R
* Champ: MSH-9
  * Contenu: Type du messageMDM^T02^MDM_T02MDM^T10^MDM_T02MDM^T04^MDM_T02
  * Type donnée: MSG
  * Caractère optionnel/obligatoire: R 
* Champ: MSH-10
  * Contenu: Identifiant du message
  * Type donnée: ST
  * Caractère optionnel/obligatoire: R
* Champ: MSH-11
  * Contenu: Processing IdP : en productionT : message de testD : environnement de debug
  * Type donnée: PT
  * Caractère optionnel/obligatoire: R
* Champ: MSH-12
  * Contenu: Version du standard 2.6
  * Type donnée: VID
  * Caractère optionnel/obligatoire: R
* Champ: MSH-17
  * Contenu: FRA
  * Type donnée: ID
  * Caractère optionnel/obligatoire: R
* Champ: MSH-18
  * Contenu: Jeux de caractères, valeurs possibles :UNICODE UTF-8 ou 8859/15
  * Type donnée: ID
  * Caractère optionnel/obligatoire: R
* Champ: MSH-21
  * Contenu: Identifiant du profil de messageMSH-21.1 : Entity Identifier (1.1)MSH-21.2 : Namespace IdCISIS_CDA_HL7_LPS
  * Type donnée: EI
  * Caractère optionnel/obligatoire: R

###### Exemples

Entête MSH d’un message MDM émis par le GESTIONNAIRE :

`MSH|^~\&|PFI|CHU_X|DPI|CHU_X|202310030830||MDM^T02^MDM^T02^MDM_T02|12345|P|2.6|||||FRA|8859/15|||1.1^ CISIS_CDA_HL7_LPS`

##### Les données concernant le patient et la venue du patient

Le message HL7 MDM est centré sur un seul patient. Les informations concernant le patient sont décrites par le segment requis PID. Le segment PV1, requis dans le standard, représente la venue courante du patient.

Ces deux segments doivent être renseignés conformément à la spécification « [PAM – National extension France » version 2.11](https://www.interopsante.org/publications) publiée en 2024. Si l’INS est véhiculé, le segment PID doit suivre les contraintes décrites dans l’[annexe CI-SIS « Prise en charge de l’identifiant National de Santé (INS) dans les standards d’interopérabilité et les volets du CI-SIS »](https://esante.gouv.fr/annexe-prise-en-charge-de-lins-dans-les-volets-du-ci-sis).

* Champ: PID-3
  * Contenu: Identifiants du patient
  * Type donnée: CX
  * Caractère optionnel/obligatoire: R
* Champ: PID-5
  * Contenu: Nom du patient
  * Type donnée: XPN
  * Caractère optionnel/obligatoire: R

Le PID-3 doit être identique aux identifiants de patient portés par le document CDA (recordTarget/patientRole/id).

Pour le segment PV1, ce volet ajoute les contraintes suivantes :

* Champ: PV1-2
  * Contenu: Classe du patient : N (Not applicable)
  * Type donnée: IS
  * Caractère optionnel/obligatoire: R

##### Le segment ORC

* Composition du segment ORC : Usage = Required / Cardinalité = [1..1]: Elément requis :
  * ?: Description :
  * ?: Valeur :
* Composition du segment ORC : Usage = Required / Cardinalité = [1..1]: **Segment ORC**
  * ?: **Common Order**
  * ?:  
* Composition du segment ORC : Usage = Required / Cardinalité = [1..1]: ORC-1
  * ?: Order control
  * ?: NW (New order/service dans le cas d'une demande d'intégration de document(s)RO (Replace order) dans le cas d'une demande de remplacementCA (Canceled) dans le cas d'une demande de suppression

##### Le segment OBR

* Composition du segment OBR : Usage = Required / Cardinalité = [1..1]: Elément requis :
  * ?: Description :
  * ?: Valeur :
* Composition du segment OBR : Usage = Required / Cardinalité = [1..1]: **Segment OBR**
  * ?: **Observation Request**
  * ?:  
* Composition du segment OBR : Usage = Required / Cardinalité = [1..1]: OBR-4
  * ?: Universal Service Identifier
  * ?:  
* Composition du segment OBR : Usage = Required / Cardinalité = [1..1]: >OBR-4.1
  * ?: Code du document
  * ?: Utiliser le [JDV_J07-XdsTypeCode-CISIS](https://ansforge.github.io/IG-terminologie-de-sante/ig/main/ValueSet-JDV-J07-XdsTypeCode-CISIS.html) de la Nomenclature des Objets de Santé (NOS).A noter qu'en cas d'envoi au DMP, le Gestionnaire doit contrôler que le type de document appartient au jeu de valeur défini par le DMP ([JDV_J66-TypeCode-DMP](https://ansforge.github.io/IG-terminologie-de-sante/ig/main/ValueSet-JDV-J66-TypeCode-DMP.html)).
* Composition du segment OBR : Usage = Required / Cardinalité = [1..1]: >OBR-4.2
  * ?: Libellé du document
* Composition du segment OBR : Usage = Required / Cardinalité = [1..1]: >OBR-4.3
  * ?: Système de codage dont est issu le code
  * ?: LN ou TRE_A05[ (lien vers la TRE)](https://ansforge.github.io/IG-terminologie-de-sante/ig/main/CodeSystem-TRE-A05-TypeDocComplementaire.html) en fonction de l'appartenance du code à l'un des trois systèmes de codage

##### Les données d’entête du document – Segment TXA

Le message MDM requiert l’utilisation du segment TXA qui porte les métadonnées associées au document contenu dans le message. Les contraintes apportées par ce volet sur le segment TXA sont les suivantes :

* Champ: TXA-1
  * Contenu: Set-ID TXA. Valeur = 1
  * Type donnée: SI
  * Caractère optionnel/obligatoire: R
* Champ: TXA-2
  * Contenu: Type de document dont les valeurs sont à prendre dansle [JDV_J07-XdsTypeCode-CISIS](https://ansforge.github.io/IG-terminologie-de-sante/ig/main/ValueSet-JDV-J07-XdsTypeCode-CISIS.html) de la Nomenclature des Objets de Santé (NOS).Par exemple : 11502-2
  * Type donnée: IS
  * Caractère optionnel/obligatoire: R
* Champ: TXA-3
  * Contenu: Document Content PresentationTEXT
  * Type donnée: ID
  * Caractère optionnel/obligatoire: R
* Champ: TXA-12 *(Note 1)*
  * Contenu: Unique document numberSi ClinicalDocument/id@extension est renseigné : ex : 58132^^1.2.250.2345.3245.13^ISOSi ClinicalDocument/id@extension n'est pas renseigné : ex : 1.2.250.2345.3245.13.58132
  * Type donnée: EI
  * Caractère optionnel/obligatoire: R
* Champ: TXA-13 *(Note 1)*
  * Contenu: Parent document numberSi ClinicalDocument/id@extension est renseigné : ex : 58131^^1.2.250.2345.3245.13^ISOSi ClinicalDocument/id@extension n'est pas renseigné : ex : 1.2.250.2345.3245.13.58131
  * Type donnée: EI
  * Caractère optionnel/obligatoire: C (Requis dans le cas d'une demande de remplacement)
* Champ: TXA-17
  * Contenu: Document completion status dont la valeur est à prendre dans la table HL7 0271AU
  * Type donnée: ID
  * Caractère optionnel/obligatoire: R

**(Note 1)** : **conformément au volet de **Structuration minimale des documents de santé**, l’identifiant du document au sein du document CDA s’exprime soit par un OID complet identifiant complètement l’instance du document (sans extension), soit par une racine d’OID commune à toutes les instances de documents de l’émetteur associée à une extension propre à l’instance du document.**

La règle de peuplement des sous champs des champs TXA-12 et TXA-13 est la suivante :

* si ClinicalDocument/id@extension est renseigné :
* si ClinicalDocument/id@extension n’est pas renseigné :

##### Les données concernant la demande de traitement sur le document

###### Le groupe de segments OBXNTE portant le document CDA

Le message HL7 MDM contient un premier groupe OBXNTE composé :

* d’un segment OBX contenant un document encodé en Base64 dont le type MIME est précisé en OBX-5.2, il peut s’agir d’un document CDA-R2 Niv1 ou d’un CDA-R2 Niv3,
* d’un segment PRT requis, pré-adopté de HL7v2.9, véhiculant les informations sur l’expéditeur du courriel MSSanté,
* d’un segment PRT requis si connu et répétable, pré-adopté de HL7v2.9, véhiculant les informations sur le(s) destinataire(s) du courriel MSSanté,
* d’un segment PRT optionnel et répétable, pré-adopté de HL7v2.9, l’(es) adresse(s) mail sur la(les)quelle(s) le(s) destinataire(s) peut ou peuvent répondre.

Les champs des segments PRT doivent être renseignés conformément aux spécifications [« Contraintes sur les types de données HL7 v2.5 applicables aux profils d’intégration du cadre technique IT Infrastructure dans le périmètre d’IHE France » release 1.8](https://www.interopsante.org/publications).

Les tableaux suivants listent l’ensemble des **segments et des champs à renseigner obligatoirement**, dans l’ordre indiqué, à l’exception du dernier segment PRT permettant de préciser l’adresse mail de réponse (qui est optionnel). Seuls les segments et les champs indiqués dans les tableaux suivants sont à renseigner dans le message MDM :

* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: Elément requis :
  * ?: Description :
  * ?: Valeur :
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: **Segment OBX**
  * ?: **Observation/Result**
  * ?: Contient un document au format CDA-R2 
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-1
  * ?: Set Id - Obx
  * ?: Numéro de séquence du segment1
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-2 
  * ?: Value Type
  * ?: ED (Encapsuled Data)
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-3 = OBR-4
  * ?: Observation Identifier
  * ?: ** **
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.1 : 
  * ?: Code du Document
  * ?: Utiliser le [JDV_J07-XdsTypeCode-CISIS](https://ansforge.github.io/IG-terminologie-de-sante/ig/main/ValueSet-JDV-J07-XdsTypeCode-CISIS.html) de la Nomenclature des Objets de Santé (NOS)
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.2 : 
  * ?: Libellé du Document
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: >OBX-3.3
  * ?: Système de codage dont est issu le code
  * ?: LN ou TRE_A05[ (lien vers la TRE)](https://ansforge.github.io/IG-terminologie-de-sante/ig/main/CodeSystem-TRE-A05-TypeDocComplementaire.html) en fonction de l'appartenance du code à l'un de ces systèmes de codage.
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-5 
  * ?: Observation Value
  * ?:  
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.1
  * ?: Source Application
  * ?:  
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.2
  * ?: Type
  * ?: text
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.3
  * ?: Data Subtype
  * ?: Le champ prend la valeur XML.
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.4
  * ?: Encoding
  * ?: Base64
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.5
  * ?: Data
  * ?: Intégrer le document CDA
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-11
  * ?: Observation Result Status
  * ?: Statut du document pris dans la table HL7 0085 (Observation Result Status Codes Interpretation)· F : Document validé· D : Document à supprimer· C : Remplacement du Document
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: **Segment PRT (Requis)**
  * ?: **Participation Information Expéditeur**
  * ?: Ce segment contient les informations de l'expéditeur à l'origine de la demande de traitement sur le document.
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-2 
  * ?: Action Code
  * ?: UC (Unchanged)
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-4 
  * ?: Participation
  * ?:  
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-4.1
  * ?: Code 
  * ?: SB
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-4.2
  * ?: Libellé du code
  * ?: Send by
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-4.3
  * ?: Name Of Coding System
  * ?: participation
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-5 (Requis si connu)
  * ?: Participation Person
  * ?: Ce champ est requis si connu si l'expéditeur est un professionnel de santé (Note 1).
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-5.1 (Requis si connu)
  * ?: ID number
  * ?: Identifiant du professionnel de santé expéditeur
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-5.2 (Requis si connu)
  * ?: Family Name
  * ?: Nom d'exercice de l'expéditeur
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-5.3 (Requis si connu)
  * ?: Given Name
  * ?: Prénom d'exercice de l'expéditeur
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-5.9 (Requis si connu)
  * ?: Assigning Authority
  * ?: Autorité d'affectation de l'identifiant de l'expéditeur 
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-5.13 (Conditionnel)
  * ?: Identifier Type Code
  * ?: Le type d'identifiant (issu de la [Table 0203 - Interop'Santé](https://www.interopsante.org/publications) présent dan le document "Contraintes sur les types de données HL7 v2.5 applicables aux profils d’intégration du cadre technique IT Infrastructure dans le périmètre d’IHE France") est requis lorsque le PRT-5.1 est renseigné
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-8 (Requis si connu)
  * ?: Participation Organization
  * ?: Ce champ est requis si connu si l'expéditeur est une organisation (Note 1).
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-8.1 (Requis si connu)
  * ?: OrganizationName
  * ?: Nom de l'organisation
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-8.6 (Requis si connu)
  * ?: Assigning Authority
  * ?: Autorité d'affectation de l'identifiant de l'organisation expéditrice du document
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-8.7 (Requis si connu)
  * ?: Identifier Type Code
  * ?: Type d'identifiant (issu de la [Table 0203 - Interop'Santé](https://www.interopsante.org/publications) présent dan le document "Contraintes sur les types de données HL7 v2.5 applicables aux profils d’intégration du cadre technique IT Infrastructure dans le périmètre d’IHE France")
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-8.10 (Requis si connu)
  * ?: Organization number
  * ?: Identifiant de l'organisation expéditrice du document
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-10 (Conditionnel)
  * ?: Participation Device
  * ?: Ce champ est requis si l'expéditeur est une application.
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-10.1
  * ?: Entity Identifier
  * ?: Identifiant de l'application
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-15 (Requis)
  * ?: Participant Telecommunication Address
  * ?:  
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-15.3
  * ?: Telecommunication Equipment Type
  * ?: X.400 (X.400 email address)
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-15.4
  * ?: Communication Address
  * ?: Intégrer l'adresse mail de l'expéditeur
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: **Segment PRT (Requis si connu)**
  * ?: **Participation Information Destinataire**
  * ?: Contient les informations du destinataire initial du courriel MSSanté. Cf (Note 1), (Note 2).
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-2 
  * ?: Action Code
  * ?: UC (Unchanged)
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-4 
  * ?: Participation
  * ?:  
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-4.1
  * ?: Code 
  * ?: RCT
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-4.2
  * ?: Libellé du code
  * ?: Result Copies To
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-4.3
  * ?: Name Of Coding System
  * ?: participation
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-5 (Requis si connu)
  * ?: Participation Person
  * ?: Ce champ est requis si connu si le destinataire initial du courriel est un PS
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-5.1 (Requis si connu)
  * ?: ID number
  * ?: Identifiant du destinataire
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-5.2 (Requis si connu)
  * ?: Family Name
  * ?: Nom d'exercice du destinataire
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-5.3 (Requis si connu)
  * ?: Given Name
  * ?: Prénom d'exercice du destinataire
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-5.9 (Requis si connu)
  * ?: Assigning Authority
  * ?: Autorité d'affectation de l'identifiant du destinataire
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-5.13 (Conditionnel)
  * ?: Identifier Type Code
  * ?: Le type d'identifiant (issu de la [Table 0203 - Interop'Santé](https://www.interopsante.org/publications) présent dan le document "Contraintes sur les types de données HL7 v2.5 applicables aux profils d’intégration du cadre technique IT Infrastructure dans le périmètre d’IHE France") est requis lorsque le PRT-5.1 est renseigné
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-8 (Requis si connu)
  * ?: Participation Organization
  * ?: Ce champ permet de faciliter le traitement du document dans la bonne organisation au niveau du système CONSOMMATEUR (service, UF, pôle…). Cf (Note 3).
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-8.1 (Requis si connu)
  * ?: OrganizationName
  * ?: Nom du destinataire
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-8.6 (Requis si connu)
  * ?: Assigning Authority
  * ?: Autorité d'affectation de l'identifiant du destinataire
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-8.7 (Requis si connu)
  * ?: Identifier Type Code
  * ?: Type d'identifiant (issu de la [Table 0203 - Interop'Santé](https://www.interopsante.org/publications) présent dan le document "Contraintes sur les types de données HL7 v2.5 applicables aux profils d’intégration du cadre technique IT Infrastructure dans le périmètre d’IHE France")
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-8.10 (Requis si connu)
  * ?: Organization number
  * ?: Identifiant du destinataire
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-15 (Requis)
  * ?: Participant Telecommunication Address
  * ?:  
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-15.3
  * ?: Telecommunication Equipment Type
  * ?: X.400 (X.400 email address)
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-15.4
  * ?: Communication Address
  * ?: Intégrer l'adresse MSSanté du destinataire
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: **Segment PRT (segment optionnel)**
  * ?: **Participation Information adresse de réponse**
  * ?: Ce segment optionnel permet d'indiquer l'adresse mail sur laquelle le destinataire peut répondre.
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-2 
  * ?: Action Code
  * ?: UC (Unchanged)
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-4 
  * ?: Participation
  * ?:  
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-4.1
  * ?: Code 
  * ?: REPLY
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-4.2
  * ?: Libellé du code
  * ?: Reply To
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-4.3
  * ?: Name Of Coding System
  * ?: participation
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: PRT-15 
  * ?: Participant Telecommunication Address
  * ?:  
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-15.3
  * ?: Telecommunication Equipment Type
  * ?: X.400 (X.400 email address)
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > PRT-15.4
  * ?: Communication Address
  * ?: Intégrer l'adresse mail de réponse

****Note 1 :** le renseignement des informations concernant l’identification de l’expéditeur/destinataire est conditionné à la capacité du GESTIONNAIRE à interroger l’annuaire de l’établissement.**

****Note 2 :** en cas de transfert du courriel original au niveau de l’établissement destinataire, il n’est pas certain que l’acteur GESTIONNAIRE puisse récupérer l’information concernant le destinataire initial du courriel. Cette information peut être utilisée pour notifier au niveau du système CONSOMMATEUR, le PS ou le service clinique concerné par le courriel (organisation) du résultat du traitement réalisé sur le document par le système CONSOMMATEUR.**

****Note 3 :** dans la configuration où le GESTIONNAIRE est en capacité de maintenir une table de correspondance entre une BAL et une organisation correspondante (service clinique, UF, pôle…), le champ PRT-8 permet de préciser l’organisation de l’établissement concerné par la demande de traitement sur le document au niveau du CONSOMMATEUR. Dans le cas où le GESTIONNAIRE n’est pas en capacité de maintenir cette table de correspondance, le système CONSOMMATEUR peut prévoir un paramétrage pour associer une organisation de l’établissement (service clinique, UF, pôle…) à une BAL afin de réaliser le traitement sur le document dans la bonne organisation.**

###### Le groupe de segments portant les informations du courriel MSSanté

* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: Elément requis :
  * ?: Description :
  * ?: Valeur :
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: **Segment OBX**
  * ?: **Observation/Result**
  * ?: Contient les informations du courriel MSSanté dont a été extrait le document
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-1
  * ?: Set Id - Obx
  * ?: Numéro de séquence du segment2
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-2
  * ?: Value Type
  * ?: ED (Encapsulated Data)
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-3 
  * ?: Observation Identifier
  * ?:  
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.1 : 
  * ?: Identifier
  * ?: Identifiant unique du courriel correspondant à l'élément Message-ID de l'entête du courriel MSSanté
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.2 : 
  * ?: Text
  * ?: Objet du courriel
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-4 
  * ?: Observation Sub-id
  * ?:  
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-5 
  * ?: Observation Value
  * ?: Contenu du courriel codé en base 64 
* Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-11
  * ?: Observation Result Status
  * ?: Valeur fixée à « F »

###### Groupes OBXNTE portant les métadonnées MSSanté

Cette section présente uniquement les métadonnées de restriction indispensables aux échanges avec la MSSanté. Ces groupes sont conformes à ceux définis dans le volet « Transmission de documents CDA en HL7v2 » version 2.1

Les métadonnées peuvent être valorisées avec Y ou N suivant qu’elles sont activées ou non au moment de la validation du document.

Ces métadonnées sont requises et doivent apparaître dans le message MDM dans l’ordre présenté ci-dessous.

Pour l’ensemble des OBX listés dans cette section, le champ OBX-3 prend ses valeurs dans la [table « MetaDMP/MSS »](meta-dmp-mss.md). Le champ OBX-11 étant requis par le standard HL7v2, la valeur de ce champ est arbitrairement fixée à « F ».

**Document Masqué aux professionnels de Santé**

Cet OBX permet au Consommateur de vérifier que le document n’est pas masqué aux professionnels de santé.

* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: Elément requis :
  * ?: Description :
  * ?: Valeur :
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: **Segment OBX**
  * ?: **Observation/Result**
  * ?:  
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-1
  * ?: Set Id - Obx
  * ?: Numéro de séquence du segment3
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-2
  * ?: Value Type
  * ?: CWE (Coded with Exceptions)
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-3
  * ?: Observation Identifier
  * ?: ** **
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.1 : 
  * ?: Code :
  * ?: MASQUE_PS
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.2 : 
  * ?: Libellé :
  * ?: Masqué aux professionnels de Santé
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.3 :
  * ?: Name of Coding system
  * ?: MetaDMPMSS
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-5
  * ?: Observation Value
  * ?:  
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.1
  * ?: Code :
  * ?: Table HL7 : 0136 :· N (No) à MASQUE_PS non Actif· Y (Yes) à MASQUE_PS Actif
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.3
  * ?: Name Of Coding System
  * ?: expandedYes-NoIndicator
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-11
  * ?: Observation Result Status
  * ?: Valeur fixée à « F » 

**Document Non visible par le patient**

Cet OBX permet d’informer le Consommateur que le document est masqué ou non au patient.

* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: Elément requis :
  * ?: Description :
  * ?: Valeur :
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: **Segment OBX**
  * ?: **Observation/Result**
  * ?: ** **
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-1
  * ?: Set Id - Obx
  * ?: Numéro de séquence du segment4
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-2
  * ?: Value Type
  * ?: CWE (Coded with Exceptions)
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-3
  * ?: Observation Identifier
  * ?: ** **
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.1 : 
  * ?: Code :
  * ?: INVISIBLE_PATIENT
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.2 : 
  * ?: Libellé :
  * ?: Document Non Visible par le patient
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.3 :
  * ?: Name of Coding system
  * ?: MetaDMPMSS
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-5
  * ?: Observation Value
  * ?:  
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.1
  * ?: Code :
  * ?: Table HL7 : 0136 :· Y (YES) à INVISIBLE_PATIENT actif· N (No) à INVISIBLE_PATIENT non actif
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.3
  * ?: Name Of Coding System
  * ?: expandedYes-NoIndicator
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-11
  * ?: Observation Result Status
  * ?: Valeur fixée à « F » 

**Document Non visible par les représentants légaux du patient**

Cet OBX permet d’informer le Consommateur que le document est masqué ou non aux représentants légaux du patient.

* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: Elément requis :
  * ?: Description :
  * ?: Valeur :
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: **Segment OBX**
  * ?: **Observation/Result**
  * ?:  
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-1
  * ?: Set Id - Obx
  * ?: Numéro de séquence du segment5
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-2
  * ?: Value Type
  * ?: CWE (Coded with Exceptions)
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-3
  * ?: Observation Identifier
  * ?: ** **
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.1 : 
  * ?: Code :
  * ?: INVISIBLE_ REP_LEGAUX
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.2 : 
  * ?: Libellé :
  * ?: Non visible par les représentants Légaux du patient
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.3 :
  * ?: Name of Coding system
  * ?: MetaDMPMSS
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-5
  * ?: Observation Value
  * ?:  
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.1
  * ?: Code :
  * ?: Table HL7 : 0136 :· Y (YES) à INVISIBLE_ REP_LEGAUX actif· N (No) à INVISIBLE_ REP_LEGAUX non actif
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.3
  * ?: Name Of Coding System
  * ?: expandedYes-NoIndicator
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-11
  * ?: Observation Result Status
  * ?: Valeur fixée à « F » 

**Modification Confidentiality Code**

Cet OBX permet d’informer le Consommateur que la transaction porte une modification du CONFIDENTIALITY CODE indiquant une mise à jour de la métadonnée de mise en visibilité du document au patients et/ou aux représentants légaux.

* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: Elément requis :
  * ?: Description :
  * ?: Valeur :
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: **Segment OBX**
  * ?: **Observation/Result**
  * ?:  
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-1
  * ?: Set Id - Obx
  * ?: Numéro de séquence du segment6
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-2
  * ?: Value Type
  * ?: CWE (Coded with Exceptions)
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-3
  * ?: Observation Identifier
  * ?: ** **
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.1 : 
  * ?: Code :
  * ?: MODIF_CONF_CODE
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.2 : 
  * ?: Libellé :
  * ?: Modification Confidentiality Code
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-3.3 :
  * ?: Name of Coding system
  * ?: MetaDMPMSS
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-5
  * ?: Observation Value
  * ?:  
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.1
  * ?: Code :
  * ?: Table HL7 : 0136 :- Y (Yes) à MODIF_CONF_CODE actif- N (No) à MODIF_CONF_CODE non Actif
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: > OBX-5.3
  * ?: Name Of Coding System
  * ?: expandedYes-NoIndicator
* Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]: OBX-11
  * ?: Observation Result Status
  * ?: Valeur fixée à « F » 

Un exemple est disponible [ici](exemples.md).

#### Le message d’acquittement HL7v2

##### Profil du message ACK

Le profil du message ACK est le suivant :

| | | | | |
| :--- | :--- | :--- | :--- | :--- |
| MSH | Message header | R | [1..1] | 2 |
| [{SFT}] | Software segment | O | [0..*] | 2 |
| [UAC] | User Authentication Credential | O | [0..1] | 2 |
| MSA | Message Acknowledgement | R | [1..1] | 2 |
| [{ERR}] | Error | C | [0..*] | 2 |

##### Structure fonctionnelle du message

Après réception du message MDM, le LPS (DPI ou RIS dans le contexte SEGUR vague 2) va acquitter le message. Ci-dessous la structure du message ACK :

**Figure 15 : Description fonctionnelle du message ACK**

 Ces segments doivent être conformes au standard HL7v2.6.

##### Description des contraintes à appliquer sur le message ACK

###### Segment MSH

Le segment MSH reprend une partie des informations du message initial :

* Message initial: Champ
  * Message d'acquittement: Description
  * ?: Champ
  * ?: Description
* Message initial: [MSH.3](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.3) - Sending Application​
  * Message d'acquittement: Application source du message à acquitter
  * ?: [MSH.5](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.5) - Receiving Application​
  * ?: Application destinatrice de l'acquittement
* Message initial: [MSH.4](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.4) - Sending Facility​
  * Message d'acquittement: Facility source du message à acquitter
  * ?: [MSH.6](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6) - Receiving Facility​
  * ?: Etablissement destinataire de l'acquittement
* Message initial: [MSH.5](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.5) - Receiving Application​
  * Message d'acquittement: Application destinatrice du message à acquitter
  * ?: [MSH.3](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.3) - Sending Application​
  * ?: Application source de l'acquittement
* Message initial: [MSH.6](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6) - Receiving Facility​
  * Message d'acquittement: Facility destinatrice du message à acquitter
  * ?: [MSH.4](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.4) - Sending Facility​
  * ?: Etablissement source de l'acquittement
* Message initial: [MSH.11](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.11) - Processing Id​
  * Message d'acquittement: Identifiant de traitement
  * ?: [MSH.11](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.11) - Processing Id​
  * ?: Identifiant de traitement

Le champ MSH.9 « Message type » prend la valeur : `ACK^T02^ACK` ou `ACK^T04^ACK` ou `ACK^T10^ACK` selon l’évènement du message initial.

* Champ: MSH-1
  * Contenu: | séparateur de champ
  * Type donnée: ST
  * Caractère optionnel/obligatoire: R
* Champ: MSH-2
  * Contenu: ^~\& : séparateur de composant, répétition, caractère d'échappement, séparateur de sous-composants
  * Type donnée: ST
  * Caractère optionnel/obligatoire: R
* Champ: MSH-3
  * Contenu: Application émettrice
  * Type donnée: HD
  * Caractère optionnel/obligatoire: R
* Champ: MSH-4
  * Contenu: Organisation émettrice
  * Type donnée: HD
  * Caractère optionnel/obligatoire: R
* Champ: MSH-5
  * Contenu: Application réceptrice
  * Type donnée: HD
  * Caractère optionnel/obligatoire: R
* Champ: MSH-6
  * Contenu: Organisation réceptrice
  * Type donnée: HD
  * Caractère optionnel/obligatoire: R
* Champ: MSH-7
  * Contenu: Date/time du message
  * Type donnée: TS
  * Caractère optionnel/obligatoire: R
* Champ: MSH-9
  * Contenu: Type du message, selon l'évènement du message initial :ACK^T02^ACKACK^T04^ACKACK^T10^ACK 
  * Type donnée: MSG
  * Caractère optionnel/obligatoire: R 
* Champ: MSH-10
  * Contenu: Identifiant du message
  * Type donnée: ST
  * Caractère optionnel/obligatoire: R
* Champ: MSH-11
  * Contenu: Processing IdP : en productionT : message de testD : environnement de debug
  * Type donnée: PT
  * Caractère optionnel/obligatoire: R
* Champ: MSH-12
  * Contenu: Version du standard 2.6 pour MDM
  * Type donnée: VID
  * Caractère optionnel/obligatoire: R
* Champ: MSH-17
  * Contenu: FRA
  * Type donnée: ID
  * Caractère optionnel/obligatoire: R
* Champ: MSH-18
  * Contenu: Jeux de caractères, valeurs possibles :UNICODE UTF-8 ou 8859/15
  * Type donnée: ID
  * Caractère optionnel/obligatoire: R

###### Segment MSA

Le segment MSA contient à minima les champs suivants :

* Champ requis: [MSA.1](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6) - Acknowledgment Code
  * Contenu: Code d'acquittement du message :· AA (Original mode: Application Accept - Enhanced mode: Application acknowledgment: Accept) : le message a été compris et intégré par l'application destinatrice qui prend la responsabilité du message et libère ainsi l'application productrice de toute obligation de le renvoyer.· AE (Original mode: Application Error - Enhanced mode: Application acknowledgment: Error) : le message contient des erreurs de syntaxe. · AR (Original mode: Application Reject - Enhanced mode: Application acknowledgment: Reject) : le message est rejeté pour une raison circonstancielle. Il peut être réémis plus tard. 
* Champ requis: [MSA.2](https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6) - Message Control Id
  * Contenu: Rappel l'identifiant du message acquitté correspondant au champ MSH.10 du message initial.

###### Segment ERR

Ce segment est utilisé au niveau des messages d’acquittement HL7 dans le cas où le champ MSA-1 prend la valeur AE (Application error).

Le tableau ci-dessous liste les champs à renseigner pour le segment ERR :

* Champ: ERR-2
  * Contenu: Localisation de l'erreur dans le cas d'une erreur de syntaxe du message initial.
  * Type donnée: ERL
  * Caractère optionnel/obligatoire: O
* Champ: ERR-3
  * Contenu: Code erreur HL7 dont les valeurs sont à prendre dans la table HL7 0357 (nom symbolique : messageErrorCondition)
  * Type donnée: CWE
  * Caractère optionnel/obligatoire: R(Note 1) (Note 2)
* Champ: ERR-4
  * Contenu: Sévérité de l'erreur dont les valeurs sont à prendre dans la table HL7 0516 (nom symbolique : errorSeverity)
  * Type donnée: ID
  * Caractère optionnel/obligatoire: R
* Champ: ERR-5
  * Contenu: Code erreur du traitement applicatif du message HL7 dont les valeurs sont à prendre dans la table user-defined 0533 (nom symbolique : applicationErrorCode)
  * Type donnée: CWE
  * Caractère optionnel/obligatoire: C(Note 1) (Note 2)

****(Note 1) :** les valeurs possibles pour les champs ERR-3 et ERR-5 sont listées dans les tables messageErrorCondition et applicationErrorCondition précisées [ici](error-codes.md).**

****Note (2) :** dans le cas où le rejet du message HL7 MDM est dû à un problème applicatif au niveau du CONSOMMATEUR, le champ ERR-3 sera renseigné avec la valeur « 207 » (Application error) et le champ ERR-5 sera renseigné avec une valeur comprise dans la table applicationErrorCode. Dans le cas où le message MDM est rejeté par le système CONSOMMATEUR pour une raison technique, le champ ERR-3 sera renseigné avec une valeur comprise dans la table messageErrorCondition et le champ ERR-5 ne sera pas renseigné.**

###### Exemple

Entête MSH d’un message MDM émis par le GESTIONNAIRE vers le CONSOMMATEUR :

```
MSH|^~\&|PFI|CHU_X|DPI|CHU_X|202310030830||MDM^T02^MDM_T02|12345|P|2.6|||||FRA|8859/15|||1.1^ CISIS_CDA_HL7_LPS

```

Un acquittement positif retourné par le CONSOMMATEUR :

```
MSH|^~\&|DPI|CHU_X|PFI|CHU_X|202310030831||ACK^T02^ACK|12346|P|2.6|||AL|AL|FRA|8859/15
MSA|AA|12345

```

Un acquittement négatif retourné par le CONSOMMATEUR : version d’HL7 inconnue

```
MSH|^~\&|DPI|CHU_X|PFI|CHU_X|202310030831||ACK^T02^ACK|12347|P|2.6|||AL|AL|FRA|8859/15
MSA|AE|12345
ERR||MSH^1^12|203^Unsupported version id^messageErrorCondition|E

```

Un acquittement négatif retourné par le CONSOMMATEUR : patient inconnu du DPI (erreur applicative)

```
MSH|^~\&|DPI|CHU_X|PFI|CHU_X|202310030831||ACK^T02^ACK|12347|P|2.6|||AL|AL|FRA|8859/15
MSA|AE|12345
ERR||PID^1^3|207^Application error^messageErrorCondition| E|902^Identifiant de patient inconnu^applicationErrorCode

```

