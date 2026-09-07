# Historique des versions - Volet Transmission au LPS de documents CDA provenant d'un courriel MSSanté v1.1.3

* [**Table of Contents**](toc.md)
* **Historique des versions**

## Historique des versions

### version 1.1.3

**Version mineure sans impact sur le développement (corrections de typo, précisions ou ajout d’informations)**

* Revue des exemples de MDN et de courriel standard, et clarification du traitement des pièces jointes ([35](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/issues/35)) 
* [Structure du MDN](struct-msg-mdn.md) : 
* ajout d’une section « Éligibilité au mécanisme MDN » rappelant les exigences `ECO.2.3.2` et `ECO.3.1.6` du [Référentiel socle MSSanté #2](https://esante.gouv.fr/espace_documentation/mssante-clients-de-messageries-securisees-de-sante/referentiel-socle-mssante-2), le périmètre d’application de ce référentiel (clients de messagerie MSSanté, à l’exclusion des webmails et des clients de messageries standards), et la conséquence sur la disponibilité du MDN — situation pour laquelle le volet prévoit le [courriel standard](struct-email-standard.md)
* précision du nombre et du rôle des parties du « multipart/report » (deux ou trois parties à rôles fixés, conformément aux [RFC 6522](https://datatracker.ietf.org/doc/html/rfc6522#section-4) et [RFC 8098](https://datatracker.ietf.org/doc/html/rfc8098#section-3)), et énoncé du besoin fonctionnel associé
* précision de l’emplacement des pièces jointes du courriel d’origine : elles sont restituées dans la troisième partie `message/rfc822`, qui contient le courriel d’origine dans son intégralité
* ajout d’un tableau précisant les valeurs attendues des champs `From:`, `To:`, `Original-Recipient:` et `Final-Recipient:` dans le contexte MSSanté
* ajout du champ `Error:` ([RFC 8098 §3.2.7](https://datatracker.ietf.org/doc/html/rfc8098#section-3.2.7)), recommandé pour porter le code et le libellé de l’erreur, et point d’attention sur la non-conformité de la valeur `processed/Error: code erreur^libellé erreur` du champ `Disposition:` à la grammaire de la RFC 8098, cette forme étant conservée en l’état
* correction de l’exemple (délimiteurs MIME de fin de partie, entête `Content-Transfer-Encoding`, lignes vides séparant les entêtes du contenu de chaque partie, format de l’entête `Date:`, identifiants de message, jeu de caractères de la première partie) et mention de son caractère illustratif et non normatif
* corrections de typographie et de références (RFC 5322 en remplacement de la RFC 2822 obsolète, `Return-Path`, notation de l’ABNF du champ `Disposition:`), et correction du lien vers le cas d’usage en erreur
 
* [Structure d’un message de notification format courriel standard](struct-email-standard.md) : 
* précision du traitement des pièces jointes : elles figurent à la fois dans la partie `message/rfc822` restituant le courriel d’origine et comme pièces jointes du courriel de notification. Cette duplication est volontaire, et justifiée par la reprise manuelle de l’erreur par un utilisateur ; elle distingue le courriel standard du MDN, dont la structure est contrainte par les RFC 6522 et 8098
* harmonisation de l’objet de l’exemple avec le format `[KO Intégration système !][code erreur]` prescrit par le volet
* correction de typographie (« courriel standart »)
 
 

### version 1.1.2

**Version mineure sans impact sur le développement (corrections de typo, précisions ou ajout d’informations)**

* Ajout de la possibilité d’utiliser un courriel standard à la place du MDN pour la gestion des erreurs ([22](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/issues/22)) 
* ajout d’une note pour décrire le [cas d’usage](volume1.md#cas-dusage)
* ajout d’une [annexe décrivant le format du courriel standard](struct-email-standard.md)
* modification de l’[annexe décrivant le MDN](struct-msg-mdn.md) : ajout d’hyperliens et ajout du [code erreur] dans l’objet
 
* Correction du lien vers le volet InteropSanté pour la table Table 0203 dans les [profils des messages](volume2.md#le-groupe-de-segments-obxnte-portant-le-document-cda) ([28](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/issues/28))
* Ajout du code 906 ‘autres type d’erreur’ dans l’annexe [Codes erreurs de traitement du message HL7 MDM](error-codes.md) ([25](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/issues/25))

### version 1.1.1

**Version mineure sans impact sur le développement (changement de format, corrections de typo, précisions ou ajout d’informations)**

* Modification du format du volet : passage du format PDF au format guide d’implémentation ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
* Avant-propos : suppression d’une ligne vide du tableau des conventions HL7, IHE ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
* Ensemble du document : 
* remplacement de message MDN par MDN (qui signifie d’emblée Message Disposition Notification) ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
 
* Volume 1 Etude fonctionnelle 
* remplacement du terme « section » par « volume 2 » ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
* [processus de transmission initiale de document(s)](volume1.md#processus-collaboratif-demande-de-transmission-initiale-de-documents) : scénario nominal, remplacement « demande de traitement de(s) document(s) » par « demande d’intégration du document » ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
* [processus de suppression de document(s)](volume1.md#processus-collaboratif-demande-de-suppression-de-documents) : scénario nominal, remplacement « demande de suppression de(s) document(s) » par « demande de suppression du document » ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
 
* Volume 2 Etude technique 
* [Choix des standards](volume2.md#choix-des-standards) : suppression de la phrase « Les échanges MSSanté doivent prendre en compte les restrictions positionnées sur le message. (Exemple : un document avec un masquage Médecin ne doit pas être envoyé sur le mail MSSanté du médecin). » qui n’a pas de rapport avec le choix des standards. ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
* correction typos/cohérence pour le type message en MSH-9.3 dans les [profils des messages](volume2.md#eléments-de-contrôle-du-message-mdm) ([6](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/issues/6))
* [Document Masqué aux professionnels de Santé](volume2.md#document-masqué-aux-professionnels-de-santé) : métadonnée de masquage aux PS : Ajout de la valeur manquante Y (YES) ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
* Correction description des segments PRT pour ‘destinataire’ et ‘adresse mail de réponse’ dans les [profils des messages](volume2.md#le-groupe-de-segments-obxnte-portant-le-document-cda) [(9)](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/issues/9)
* Déplacement de la section LIEN ENTRE L’EN-TETE CDA ET LES METADONNEES XDS dans Volume 3 Annexes ([8](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/issues/8))
 
* Volume 3 Annexes 
* [Structure du MDN (MSSanté)](struct-msg-mdn.md) (Annexe 4) modification du titre : Structure du MDN (Message Disposition Notification) - MSSanté ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
* [exemples de messages d’acquittement](volume2.md#exemple) 
* Correction de MSH-21 (version de l’interface 1.1 au lieu de 1.2) sur le segment MSH du message initial MDM
* Suppression du champ MSH-21 (le message d’acquittement n’a pas de contraintes particulières par rapport au message spécifié dans le standard international)
 
* [Ajout du code erreur 905](error-codes.md#codes-erreurs-de-traitement-du-message-hl7-mdm) ([15](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/issues/15))
 

### Rappel de l’historique des anciennes versions au format PDF (avant novembre 2024)

Ici nous rappelons l’historique des précédentes versions. Cet historique est également disponible dans la dernière version du volet au format pdf : [ANNEXE 7 CI_SIS_TRANS_LPS_DOC_CDA_COURRIEL_MSSANTE_V1.1_Post_PAT_2023_CONCERTATION_FINAL.pdf](https://esante.gouv.fr/sites/default/files/media_entity/documents/CI_SIS_TRANS_LPS_DOC_CDA_COURRIEL_MSSANTE_V1.1_Post_PAT_2023_CONCERTATION_FINAL.pdf)

| | | | | | | | | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
|   | **Version** | **Rédigé par** | **Vérifié par** | **Validé par** | | | | | | | | | |
|   | 1.0 | Kereval | Le 13/02/2023 | ANS | Le 19/02/2023 | ANS | Le 26/04/2023 | | | | | | |
|   | Motif et nature de la modification : **Première version ** | | | | | | | | | | | | |
|   | 1.1 | ANS | Le 24/10/2023 | ANS |   | ANS |   | | | | | | |
|   | ·       Ajout de la partie Avant-propos et des questions ouvertes·       Le volet est scindé en 2 parties : Etude fonctionnelle et Etude technique·       Section 1 : suppression de toutes références au choix technique (HL7)·       Ajout de l’étude fonctionnelleo    Section 2 : Cas d’usageo    Section 3 : Organisation métiero    Section 4 : Acteurs et Transactionso    Section 5 : cas d’usageo    Section 6 : Définition des processus collaboratifso    Section 7 : Identification des flux.·       Etude techniqueo    Section 7 : Périmètre. §  Précision concernant l’accusé de lecture proposé à titre expérimental à retours des éditeurs attendus.o    Section 8 : ajout du rôle des acteurso    Section 9 : Standards§  Référence la version 1.7.4 des « Contraintes sur les types de données HL7 v2.5 applicables aux profils d’intégration du cadre technique IT Infrastructure dans le périmètre d’IHE France » qui intègre l’agrandissement du champ EI-1 du type de données EI (passage de EI-1 à 199).§  Ajout de la contrainte sur les types de données CE et CWE pré adoptée de la version 2.7 d’HL7 : nécessité de citer le code et le codeSystem dont est issu ce code.o    Section 11 : Interactions entre les acteurs, précisions apportées sur le schémao    Section 12.1.1 : ajout du profil de message MDMo    Section 12.1.2 : description fonctionnelle. §  Préciser la cardinalités sur les métadonnées [1..*]§  1° OBXNTE : supprimer la référence au CDAr2 Niv1 (MDM contient un CDA Niv1 ou Niv3)o    Section 12.2.1 : ajout des contraintes sur les éléments de contrôle MSH, MSA, ERRo    Section 12.2.2 : éléments concernant le patient PID, PV1o    Section 12.2.3 : Ajout de la description OCRo    Section 12.2.4 : Ajout de la description du segment OBRo    Section 12.2.5 : Ajout de la description du segment TXAo    Section 12.2.6 : Eléments concernant la demande de traitement sur le document§  12.2.6.1 : Le1° groupe de segment OBXNTE, les segments et les champs sont à renseigner dans l’ordre indiqué. Ajout OBX-3.3 (contrainte CWE). Reprise des champs concernant l’expéditeur et le destinataire.§  12.2.6.3 : groupe de segment portant les métadonnées. ·       Les métadonnées doivent obligatoirement être renseignées et doivent apparaître dans l’ordre indiqué. ·       Ajout des lignes OBX-3.3 pour prendre en compte la contrainte sur le type de donnée CWE (code+codeSystem dont est issu le code)§  Section 12.2.7.3 : description ERR et exempleso    Section 12.3.1 : description de l’évènement déclenchant de l’accusé de lecture dans le contexte de ce volet. Proposition de considérer cet accusé de lecture à titre expérimental à retours des éditeurs attendus. | | | | | | | | | | | | |
| 1.1 | ANS | Le 15/01/2024 | ANS | 19/01/2024 | DNS | 21/02/2024 | | | | | | | |
| Motif et nature de la modification : Prise en compte des retours de concertation publique (27/11/2023 au 08/12/2023) et prise en compte des modifications demandées par la DNS après clôture de la période de concertation publique.·       Rédaction des questions ouvertes·       Section 1.1 : référence au volet Transmission d’un document CDA provenant d’un courriel MSS de façon à mettre en exergue le lien entre le présent volet et le volet référencé·       Volume 1 – Etude fonctionnelleo   Section 2 : complétude des cas d’usage DNS et modifications en fonction des remarques de la DNSo   Section 4.1 : liste des acteurs concernés. L’envoi par le CONSOMMATEUR et la réception par le GESTIONNAIRE de l’accusé métier de lecture est supprimé (ZAM_Z03). Le GESTIONNAIRE envoie simplement l’accusé du message HL7 MDM. Cet accusé HL7 rend compte du bon déroulement ou pas de la demande de traitement du document au niveau du CONSOMMATEUR.o   Section 4.2 : Diagramme des acteurs/transactions. Suppression de l’accusé de lecture MSS (ZAM_Z03) entre l’acteur CONSOMMATEUR et l’acteur GESTIONNAIREo   Section 4.3 : regroupement de l’acteur CONSOMMATEUR avec l’acteur IHE Content Consumero   Section 5 : Processus collaboratifs. Amélioration de la rédaction des processus et suppression de la notion d’accusé métier de lecture MSS (ZAM_Z03).·       Volume 2 – Etude techniqueo   Section 7 : Périmètre de la transaction, suppression de l’accusé métier de lecture MSS (ZAM_Z03). L’accusé de lecture (message MDN) est généré par le GESTIONNAIRE sur réception de l’ack HL7 du message MDM o   Section 9 : Choix des standards§  Référencement de la version 2.11 de la version française PAM.FR§  Référencement de la version 1.8 des types de données HL7 en France (passage de la longueur du champ ED-1 de 16 caractères à 128 caractèreso   Section 11 : modification de la figure 13. La PFI génère le message MDN (MSSanté) à partir de l’ack du message HL7 MDM. Le client de messagerie de la PFI envoi cet accusé de lecture (message MDN MSSanté) à l’expéditeur.o   Section 12.2.6.1 : OBXNTE portant le document. Ajout d’une note au niveau du PRT destinataireo   Section 12.2.6.2 : Informations du courriel MSS. Le contenu du courriel est codé en base 64o   Section 12.2.6.3.5 : suppression de l’OBX permettant de préciser qu’un accusé métier de lecture MSS est attendu par le GESTIONNAIREo   Section 12.3 : suppression de la description du message ZAM^Z03^ZAM_Z01·       Annexe 2 : ajout des codes erreurs 902, 903 et 904 demandés par la DNS dans la table des codes erreurs de traitement du message MDM·       Annexe 3 : modification des exemples pour prendre en compte les corrections/modifications de la version·       Annexe 4 : structure du message MDN-Message Disposition Notification (MSSanté) | | | | | | | | | | | | | |
| 1.1 | ANS | Le 21/03/2024 | ANS |   | ANS |   | | | | | | | |
| Motif et nature de la modification : Prise en compte des retours de concertation publique (04/03/2024 au 18/03/2024.·       Ajout du paragraphe 1.2 Ce dont ne traite pas ce volet·       Volume 1 – Etude fonctionnelleo   Section 2.1 : correction de l’@ MSS du médecino   Paragraphe 2.3.1 : cas d’usage, transmission d’une BAL orga vers une BAL orga : précisions apportées sur le point d’attention juste avant la figure 4. o   Section 3.2 : les processus, précision apportée sur les métadonnées MSS sont limitées au masquage des documents aux PS et à la mise en visibilité au patient/rep légaux.·       Volume 2 – Etude techniqueo   Section 7 : Modification de la rédaction du périmètre de la transaction : « Le périmètre des spécifications s’applique à toute demande de transmission initiale/remplacement/suppression d’un document CDA-R2, provenant d’un courriel MSSanté réceptionné dans une BAL applicative et traité par la PFI de l’établissement hospitalier »o   Section 12.1.1 : §  Profil du message HL7 MDM : passage du segment PRT à obligatoire et répétable [1..*]§  Précision dans le texte sous le profilo   Section 12.2.5 : précisions apportées sur le peuplement des champs TXA-12 et TXA-13o   Section 12.2.6.1 : OBX portant le document§  Précision (*Note 2) :* il sera possible au GESTIONNAIRE ou au CONSOMMATEUR de notifier le PS ou le service d’une demande de traitement sur un document à condition que le GESTIONNAIRE ou le CONSOMMATEUR ait la capacité à maintenir une correspondance entre les BAL perso/orga/app et les PS/services correspondants.o   Section 12.2.6.3.1 : OBX masquage aux PS§  Dans le contexte de la réception d’un courriel par la PFI, la métadonnée MASQUE_PS devrait prendre la valeur « N » (exigence formulée dans le volet « Transmission de document(s) CDA en HL7v2 ». Dans le cas contraire, la PFI ne doit pas envoyer le message HL7 MDM vers le DPI.o   Section 12.2.7.3.3 : message ACK du message MDM§  Ajout du champ ERR-5 qui permet de préciser l’erreur de traitement de la demande sur le document au niveau du CONSOMMATEUR§  Précisions des noms symboliques pour les tables HL70357 et HL70516§  Précisions apportées sur le renseignement des champs ERR-3 et ERR-5·       Annexe 3 : la table initiale est scindée en deux tables : messageErrorCondition et applicationErrorCondition | | | | | | | | | | | | | |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |

