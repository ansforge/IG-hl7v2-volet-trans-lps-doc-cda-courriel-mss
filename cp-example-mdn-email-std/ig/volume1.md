# Volume 1 : Etude fonctionnelle - Volet Transmission au LPS de documents CDA provenant d'un courriel MSSanté v1.1.3

* [**Table of Contents**](toc.md)
* **Volume 1 : Etude fonctionnelle**

## Volume 1 : Etude fonctionnelle

### Cas d’usage

Cette section décrit, **à titre d’exemple et de façon non exhaustive**, un ensemble de cas d’usage. Pour une meilleure compréhension du lecteur, ces cas d’usage couvrent les échanges entre la PFI et le logiciel métier consommateur, mais également les échanges en amont de la PFI de l’établissement destinataire (et donc au-delà du périmètre du présent volet).

#### Réception et traitement par la PFI de l’établissement hospitalier d’un document clinique provenant d’un médecin traitant

**Cas d’usage :** le médecin traitant du patient, le Dr Adam Hoda, envoi un compte rendu au médecin hospitalier qui prend en charge son patient.

Le patient est connu de l’établissement hospitalier et est pris en charge par le Dr Dupont qui exerce à l’hôpital-A (jean.dupont@hopital-A.mssante.fr). Le Dr Adam Hoda valide le compte rendu et renseigne au travers de l’IHM de son logiciel métier les métadonnées de masquage aux PS et de visibilité au patient et à ses représentants légaux attachées au compte rendu. Il précise également qu’il souhaite envoyer ce compte rendu au Dr Dupont, et sélectionne à partir de son annuaire l’adresse mail de contact de ce médecin. Avant de valider sa demande, le Dr Hoda peut préciser s’il souhaite recevoir un accusé de réception MSSanté et un accusé de lecture (prise en compte de sa demande par le destinataire).

La demande du Dr Adam est détectée et interprétée par la PFI de l’établissement hospitalier. La PFI analyse le contenu du courriel et transmet au destinataire la demande de traitement à réaliser sur le document contenu dans ce courriel. Si demandé initialement, l’accusé de réception du courriel est renvoyé vers la BAL du Dr Adam Hoda suite à la réception du mail sur le serveur de messagerie de l’établissement hospitalier.

#### Réception d’un compte rendu de biologie par un établissement hospitalier

**Cas d’usage :** un établissement hospitalier (le CH Martin) réceptionne, via MSSanté, un compte rendu de laboratoire concernant un patient pris en charge dans l’établissement, provenant d’un laboratoire d’analyses externe au CH Martin. Le laboratoire d’analyse ainsi que le CH Martin sont dotés d’une PFI. Ce cas d’usage nécessite un accord de partenariat entre les deux structures permettant de rendre possible l’échange MSSanté au travers des BAL applicatives.

##### Description du cas nominal

Le médecin biologiste du laboratoire d’analyses valide le compte rendu de biologie via son système de gestion de laboratoire (SGL) et précise les métadonnées de masquage du document aux PS et de visibilité au patient et à ses représentants légaux. Ces métadonnées peuvent également, selon les organisations mises en place, être paramétrées en fonction du type d’analyse réalisé. Le SGL est également paramétré pour prendre en compte les souhaits du médecin biologiste concernant la réception des accusés métier de réception DMP, de réception MSSanté par le serveur de messagerie de l’établissement CH Martin, et l’accusé métier de lecture/traitement du courriel MSSanté et du(des) document(s) CDA contenu(s) dans la pièce jointe IHE_XDM.zip.

A la validation du compte rendu de biologie par le médecin biologiste, le SGL envoie la demande d’intégration du CR de biologie dans l’application destinatrice.

La PFI du laboratoire de biologie réceptionne la demande, construit le courriel ainsi que la pièce jointe IHE_XDM.zip et l’envoi à une BAL applicative de l’établissement CH Martin dédiée ou non à la réception des CR de biologie de laboratoire partenaire. La PFI du CH Martin détecte l’arrivée du courriel, analyse son contenu et construit la demande d’intégration du CR de biologie dans le logiciel métier du destinataire (DPI).

Le DPI intègre le document à partir des informations disponibles dans la demande d’intégration et dans l’entête du document CDA, et renvoie un accusé de réception de la demande à la PFI.

Dans le contexte SEGUR vague 2, la PFI doit pouvoir générer un courriel MDN (Message Disposition Notification) à destination de la BAL du SGL contenant le statut de l’intégration.

La structure du MDN est décrite [ici](struct-msg-mdn.md).

>  **Point d'attention :** dans le contexte du SEGUR vague 2, la PFI doit pouvoir générer un courriel MDN (Message Disposition Notification) à destination de la BAL du SGL contenant le statut de l'intégration. 

**Figure 2 : Réception d’un CR de biologie médicale – Cas nominal**

 La Figure 2 illustre les échanges de bout en bout relatifs à une demande de transmission du compte rendu du SGL d’un laboratoire extérieur vers le DPI d’un établissement partenaire.

Le diagramme serait identique dans le cas d’une demande de remplacement ou de suppression du compte rendu.

##### Description du cas en erreur

Le CR de biologie n’est pas intégré dans le logiciel métier du destinataire pour une raison technique (par exemple, non-conformité de la transaction de demande d’intégration du document) ou pour une raison fonctionnelle (par exemple, le patient n’est pas connu du logiciel destinataire).

Dans le contexte du SEGUR, la PFI doit pouvoir envoyer un accusé métier de lecture MSSanté négatif vers la BAL de l’expéditeur dans le cas où le médecin biologiste a exprimé le souhait de recevoir cet accusé de lecture MSSanté.

Sur la figure suivante, seule la partie basse de la figure précédente est représentée. Les séquences relatives à l’accusé de réception MSSanté sont identiques.

**Figure 3 : Réception d’un CR de biologie médicale – Gestion des erreurs**

 La Figure 3 illustre la gestion des erreurs par l’établissement destinataire dans le cas d’une demande de transmission du compte rendu du SGL vers le DPI.

Le diagramme serait identique dans le cas d’une demande de remplacement ou de suppression du compte rendu.

>  Dans le cas où un MDN (Message Disposition Notification) n'a pas été explicitement demandé par le destinataire (via l'entête `Disposition-Notification-To` dans le message d'origine), et que, pour pouvoir gérer toutes les erreurs, on souhaite utiliser une BAL dédiée, un courriel 'standard' peut être utlisé. La structure du courriel est précisée [ici](struct-email-standard.md). 

**Figure 3 bis: Réception d’un CR de biologie médicale - Gestion des erreurs vers une BAL dédiée**

 
 **Ce cas d'usage est hors périmètre de ce volet.** 

#### Transmission d’un document clinique d’un patient d’un établissement hospitalier vers un autre établissement hospitalier

**Cas d’usage :** Le Dr Jean Dupont exerce dans le service X de l’établissement-A. Il souhaite transférer un de ses patients dans le service Y de l’établissement B. Il demande à la secrétaire médicale du service X d’envoyer le compte rendu d’hospitalisation de son patient à l’équipe de soins du service Y de l’établissement-B.

La secrétaire médicale du service X de l’établissement-A envoie un courriel à la BAL du service Y de l’établissement-B. Les deux établissements sont dotés d’une PFI.

##### Description du cas nominal

Dans ce cas d’usage, le compte rendu d’hospitalisation est envoyé par MSSanté sur la BAL organisationnelle du service Y. La secrétaire de l’établissement-B consulte sa BAL organisationnelle. Si la secrétaire souhaite intégrer automatiquement les documents de la pièce jointe IHE_XDM.zip dans le DPI, elle transfère manuellement les courriels vers la BAL applicative du service Y. Ces courriels sont ensuite détectés par la BAL applicative de la PFI de l’établissement-B qui les traitent, construit pour chaque courriel la demande d’intégration/remplacement/suppression du document et envoie cette demande au DPI du service Y. le document est intégré/remplacé/supprimé dans le DPI du service Y.

La secrétaire médicale du service X de l’établissement-A sélectionne le compte rendu et sélectionne, à partir de l’annuaire de l’établissement, la BAL organisationnelle correspondant au service Y de l’établissement-B. elle précise également si elle souhaite recevoir en retour un accusé de réception MSSanté (réception par le serveur de messagerie de l’établissement-B) ainsi qu’un accusé de lecture MSSanté (selon les organisations, ce choix peut être réalisé par paramétrage).

Cette demande d’envoi est traitée par la PFI de l’établissement-A qui réceptionne, analyse les éléments portés par la transaction émise à partir du DPI du service X et construit l’archive IHE_XDM conformément au volet Echange de documents de santé du CI_SIS en pièce jointe du courriel à destination du service Y de l’établissement-B.

Le courriel envoyé par la BAL attachée à la PFI de l’hôpital-A est réceptionné par la BAL organisationnelle du service Y. Dans le cas d’usage décrit ci-dessous, la secrétaire du service Y de l’établissement-B prend connaissance des courriels non lus dans la BAL organisationnelle du service et transfert ces courriels vers la BAL applicative du service Y dans le cas où elle désire importer automatiquement les documents dans le DPI. Si un accusé de lecture a été demandé par l’expéditeur, celui-ci est alors renvoyé vers la BAL organisationnelle du service X de l’établissement- A. Des règles peuvent également être mises en place dans le serveur de messagerie de l’établissement-B pour transférer automatiquement les courriels avec une pièce jointe IHE_XDM.zip ou un objet qui commence par XDM/1.0/DDM vers la BAL applicative du service Y.

Suite au transfert, la PFI de l’établissement-B détecte chaque courriel arrivé sur la BAL applicative du service Y. La PFI de l’hôpital-B extrait les informations du courriel ainsi que la demande d’intégration associée au document clinique et transmet ces éléments vers le DPI associé au service Y pour traitement de la demande d’intégration du document clinique dans le dossier du patient. La configuration d’une BAL applicative par service de l’établissement B permet au DPI de classer plus finement le document.

Le DPI intègre le document à partir des informations qu’il reçoit et renvoie un accusé de réception à la PFI.

Dans le contexte du SEGUR vague 2, la PFI doit pouvoir générer un courriel MDN (Message Disposition Notification) à destination de la BAL organisationnelle du service Y contenant le statut de l’intégration du document. En cas d’erreur, la secrétaire pourra envisager une intégration manuelle (voir le paragraphe suivant).

La structure du MDN est précisée [ici](struct-msg-mdn.md).

>  **Point d'attention :** ce cas d’usage décrit un mécanisme de traitement d’un courriel réceptionné sur une BAL organisationnelle. Ce mécanisme pourrait être identique pour un courriel réceptionné sur une BAL personnelle, sous réserve de s’assurer et de respecter les exigences réglementaires relatives au transfert d’un courriel personnel dans un contexte professionnel. 

 Ce cas d’usage nécessite de définir une BAL organisationnelle ainsi qu’une BAL applicative associée pour chaque service clinique de l’établissement B. La PFI ou le DPI peuvent prévoir un paramétrage pour associer un service clinique de l’établissement à une BAL afin de classer les documents dans le bon service. 

**Figure 4 : Transmission d’un document clinique d’un patient d’un CH vers un autre CH - Cas nominal**

La Figure 4 illustre les échanges de bout en bout relatifs à une demande de transmission du compte rendu du SGL vers le DPI. Le diagramme serait identique dans le cas d’une demande de remplacement ou de suppression du compte rendu.

##### Description du cas d’usage en erreur

La cinématique des échanges est la même que précédemment mais le compte rendu d’hospitalisation n’est pas intégré dans le DPI du service Y en raison de l’inexistence du patient dans le DPI.

La figure ci-dessous représente uniquement la partie basse de la figure précédente, à partir de la lecture par la PFI de la BAL applicative de l’établissement-B.

**Figure 5 : Transmission d’un document clinique d’un patient d’un CH vers un autre CH - Gestion des erreurs**

La Figure 5 illustre la gestion des erreurs par l’établissement destinataire dans le cas d’une demande de transmission d’un compte rendu vers le DPI d’un autre établissement.

Le diagramme serait identique dans le cas d’une demande de remplacement ou de suppression du compte rendu.

>  Dans le cas où un MDN (Message Disposition Notification) n'a pas été explicitement demandé par le destinataire (via l'entête `Disposition-Notification-To` dans le message d'origine), et que, pour pouvoir gérer toutes les erreurs, on souhaite utiliser une BAL dédiée, un courriel 'standard' peut être utlisé. La structure du courriel est précisée [ici](struct-email-standard.md). 

**Figure 5 bis: Transmission d’un document clinique d’un patient d’un CH vers un autre CH - Gestion des erreurs vers une BAL dédiée**

 
 **Ce cas d'usage est hors périmètre de ce volet.** 

### Organisation du contexte métier

##### Les groupes de processus

Réception par la plateforme d’intermédiation (PFI) d’une demande de traitement sur le(s) document(s) clinique(s) relatif(s) à un patient provenant d’une Boîte aux Lettres (BAL) MSSanté, pour transmission et traitement de cette demande au niveau d’un logiciel consommateur au sein de l’établissement. Ce groupe de processus est divisé en quatre processus décrits dans les sections suivantes.

##### Les processus

Le groupe de processus est divisé en quatre processus :

* Une demande de transmission initiale de document(s) pour intégration dans le LPS,
* Une demande de remplacement de document(s) initialement envoyé(s) par MSSanté pour remplacement au niveau du LPS,
* Une demande de mise à jour des métadonnées de document(s)(*) initialement envoyé(s) par MSSanté pour mise à jour au niveau du LPS,
* Une demande de suppression de document(s) initialement envoyé(s) par MSSanté pour suppression au niveau du LPS.

(*) : **dans le contexte français, conformément au [volet Partage de documents de santé du CI_SIS](https://esante.gouv.fr/volet-partage-de-documents-de-sante), la mise à jour des métadonnées du document est limitée à la mise à jour des informations de masquage du document aux PS et de mise en visibilité du document au patient et à ses représentants légaux ainsi que le statut du document.**

**Cette mise à jour est gérée comme un remplacement de document, ce qui implique la création d’une nouvelle version de document par le système créateur de documents. Cette nouvelle version vient remplacer la précédente au niveau du consommateur (logiciel métier destinataire du courriel).**

Le nombre de processus est ainsi réduit aux trois processus synthétisés sur la Figure suivante.

Dans le contexte du SEGUR vague 2, les applications consommatrices de ces documents sont limitées au dossier patient informatisé (DPI) et au système de gestion de radiologie (RIS).

**Figure 6 : Organisation du contexte métier du volet « Transmission au LPS d'un document provenant d'un courriel »**

Le périmètre de l’étude englobe les processus en bleu sur le diagramme de paquetage.

### Acteurs et transactions

#### Liste des Acteurs et systèmes concernés

Le présent volet met en œuvre les Acteurs IHE suivants, représentant le rôle joué par un ou plusieurs composants du système d’information :

* Acteur: GESTIONNAIRE
  * Description: Le GESTIONNAIRE réceptionne et transmet au système CONSOMMATEUR les demandes de transmission initiale/remplacement/suppression de document(s) provenant d'un courriel.
* Acteur: CONSOMMATEUR
  * Description: Le CONSOMMATEUR réceptionne et gère les demandes de transmission initiale/remplacement/suppression de document(s) issues d'un courriel, provenant du système GESTIONNAIRE et renvoie l'accusé de traitement de la demande vers le GESTIONNAIRE.

Le tableau suivant liste, pour chacun des acteurs, les systèmes du SIH concernés :

* Acteur: GESTIONNAIRE
  * Systèmes concernés: - Les Plateformes d'Intermédiation (PFI) qui assurent la transmission de document(s) cliniques provenant d'un courriel MSSanté vers un CONSOMMATEUR (le LPS destinataire).
* Acteur: CONSOMMATEUR
  * Systèmes concernés: - Tout logiciel métier (LPS) du SIH qui récupère et gère la demande de traitement du document transmis par le GESTIONNAIRE.- Dans le contexte du SEGUR vague 2, les applications consommatrices de ces documents sont limitées au dossier patient informatisé (DPI) et au système de gestion de radiologie (RIS).

#### Diagramme des Acteurs/Transactions

**Figure 7 : Diagramme des Acteurs/transactions**

Le tableau ci-dessous représente l’ensemble des acteurs directement impliqués dans ce volet ainsi que les transactions entre ces acteurs.

Pour être en conformité avec ce volet, chaque acteur doit supporter les transactions obligatoires (R-Required) et peut supporter les transactions optionnelles (O-Optional).

* Acteur: GESTIONNAIRE
  * Transaction: Flux6 HL7-MDM en émission : Demande de transmission/remplacement/suppression d'un document CDA
  * **Caractère requis/optionnel**: R
* Acteur: CONSOMMATEUR
  * Transaction: Flux6 HL7-MDM en réception : Demande de transmission/remplacement/suppression d'un document CDA
  * **Caractère requis/optionnel**: R

#### Regroupement requis des Acteurs

Cette section décrit les exigences en termes de regroupement d’acteurs pour chacun des acteurs identifiés précédemment.

* Acteur de ce volet: GESTIONNAIRE
  * Groupé avec un autre acteur: Système cible (Portable Media Importer) XDM
  * Référence: [Volet Echange de documents de santé](https://esante.gouv.fr/volet-echange-de-documents-de-sante)
* Acteur de ce volet: CONSOMMATEUR
  * Groupé avec un autre acteur: Content Consumer ([TF PCC](https://www.ihe.net/uploadedFiles/Documents/PCC/IHE_PCC_TF_Vol1.pdf))
  * Référence: TF Patient Care Coordination - Appendix A: Actors definition

 

L’acteur GESTIONNAIRE est groupé avec :

* L’acteur Système cible du [volet d’Echange de documents de santé](https://esante.gouv.fr/volet-echange-de-documents-de-sante), pour permettre à la PFI de réceptionner l’archive IHE_XDM inclue dans le courriel reçu de l’extérieur,

L’acteur CONSOMMATEUR est groupé avec :

* L’acteur Content Consumer définit dans le [Technical Framework PCC d’IHE](https://www.ihe.net/uploadedFiles/Documents/PCC/IHE_PCC_TF_Vol1.pdf), permettant au CONSOMMATEUR de visualiser et d’importer tout ou parties du document CDA.

### Définition des processus collaboratifs

#### Processus collaboratif « Demande de transmission initiale de document(s) »

**Figure 9 : Processus collaboratif « Demande de transmission initiale de document(s) » pour intégration au niveau du CONSOMMATEUR**

* Service Attendu: Pré-Conditions
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande d'intégration de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: - Le patient est connu du CONSOMMATEUR.- Le GESTIONNAIRE détecte qu'un courriel a été reçu sur la BAL avec en pièce jointe une archive XDM.- Le GESTIONNAIRE dézippe l'archive XDM. Il vérifie qu'elle contient des documents de santé d'un patient au format CDA ainsi qu'un fichier de métadonnées.
* Service Attendu: Post-Conditions
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande d'intégration de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: Le GESTIONNAIRE trace les transmissions de document(s)
* Service Attendu: Contraintes fonctionnelles
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande d'intégration de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: La BAL du GESTIONNAIRE doit être en capacité de détecter les courriels entrants avec demande de traitement sur le(s) document(s)
* Service Attendu: Scénario Nominal
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande d'intégration de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: - Suite à la réception d'un courriel sur la BAL destinatrice, le GESTIONNAIRE transmet le document de santé de la pièce jointe au CONSOMMATEUR.- Le CONSOMMATEUR traite la demande d'intégration du document.- Le CONSOMMATEUR retourne au GESTIONNAIRE un accusé de réception de la demande d'intégration du document.

#### Processus collaboratif « Demande de remplacement de document(s) »

**Figure 10 : Processus collaboratif « Demande de remplacement de document(s) » au niveau du CONSOMMATEUR**

 Le processus « Demande de remplacement de document(s) » permet également de gérer la mise à jour des métadonnées associées au(x) document(s).

Ainsi, dans le cas d’une demande de mise à jour des métadonnées de masquage/démasquage aux PS et de visibilité du document au patient, une nouvelle version de document est générée par l’initiateur du courriel. Cette nouvelle version vient remplacer la précédente au niveau du CONSOMMATEUR (application métier destinatrice).

* Service Attendu: Pré-Conditions
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de remplacement de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: - Le patient est connu du CONSOMMATEUR.- Le document doit être validé et identifié comme remplaçant un document précédemment envoyé par MSSanté.- Le CONSOMMATEUR dispose de la dernière version du document original dans sa base de données.- Le GESTIONNAIRE détecte qu'un courriel a été reçu sur la BAL avec en pièce jointe une archive IHE_XDM.- Le GESTIONNAIRE dézippe l'archive XDM. Il vérifie qu'elle contient des documents de santé d'un patient au format CDA ainsi qu'un fichier de métadonnées et prend connaissance du traitement à effectuer sur le(s) document(s)
* Service Attendu: Post-Conditions
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de remplacement de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: Le GESTIONNAIRE trace les transmissions de document(s)
* Service Attendu: Contraintes fonctionnelles
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de remplacement de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: La BAL du GESTIONNAIRE doit être en capacité de détecter les courriels entrants avec demande de traitement sur le(s) document(s)
* Service Attendu: Scénario Nominal
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de remplacement de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: - Suite à la réception du courriel sur la BAL destinatrice, le GESTIONNAIRE transmet la demande de remplacement de documents de santé de la pièce jointe au CONSOMMATEUR- Le CONSOMMATEUR traite la demande de remplacement du document.- Le CONSOMMATEUR retourne au GESTIONNAIRE un accusé de réception de la demande de remplacement du document. 

#### Processus collaboratif « Demande de suppression de document(s) »

**Figure 11 : Processus collaboratif « Demande de suppression de document(s) » au niveau du CONSOMMATEUR**

* Service Attendu: Pré-Conditions
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de suppression de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: - Le patient est connu du consommateur.- Le document doit être validé et doit correspondre à la dernière version du document envoyé au CONSOMMATEUR.- Le CONSOMMATEUR dispose de la dernière version du document original dans sa base de données.- Le GESTIONNAIRE détecte qu'un courriel a été reçu sur la BAL avec en pièce jointe une archive IHE_XDM.- Le GESTIONNAIRE dézippe l'archive XDM. Il vérifie qu'elle contient des documents de santé d'un patient au format CDA ainsi qu'un fichier de métadonnées et prend connaissance du traitement à effectuer sur le document
* Service Attendu: Post-Conditions
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de suppression de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: Le GESTIONNAIRE trace les transmissions de document(s)
* Service Attendu: Contraintes fonctionnelles
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de suppression de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: La BAL du GESTIONNAIRE doit être en capacité de détecter les courriels entrants avec demande de traitement sur le(s) document(s)
* Service Attendu: Scénario Nominal
  * Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de suppression de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.: - Suite à la réception d'un courriel sur la BAL destinatrice, le GESTIONNAIRE transmet la demande de suppression du document de santé de la pièce jointe au CONSOMMATEUR- Le CONSOMMATEUR traite la demande de suppression du document.- Le CONSOMMATEUR retourne au GESTIONNAIRE un accusé de réception de suppression du document.

### Identification des flux

**Figure 12 : Identification des flux**

