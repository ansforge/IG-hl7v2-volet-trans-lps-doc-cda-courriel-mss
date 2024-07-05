Cette section décrit, **à titre d’exemple et de façon non exhaustive**, un ensemble de cas d’usage. Pour une meilleure compréhension du lecteur, ces cas d’usage couvrent les échanges entre la PFI et le logiciel métier consommateur, mais également les échanges en amont de la PFI de l’établissement destinataire (et donc au-delà du périmètre du présent volet).

### Réception et traitement par la PFI de l’établissement hospitalier d’un document clinique provenant d’un médecin traitant

**Cas d’usage :** le médecin traitant du patient, le Dr Adam Hoda, envoi un compte rendu au médecin hospitalier qui prend en charge son patient.
Le patient est connu de l’établissement hospitalier et est pris en charge par le Dr Dupont qui exerce à l’hôpital-A (jean.dupont@hopital-A.mssante.fr). Le Dr Adam Hoda valide le compte rendu et renseigne au travers de l’IHM de son logiciel métier les métadonnées de masquage aux PS et de visibilité au patient et à ses représentants légaux attachées au compte rendu. Il précise également qu’il souhaite envoyer ce compte rendu au Dr Dupont, et sélectionne à partir de son annuaire l’adresse mail de contact de ce médecin. Avant de valider sa demande, le Dr Hoda peut préciser s’il souhaite recevoir un accusé de réception MSSanté et un accusé de lecture (prise en compte de sa demande par le destinataire).
La demande du Dr Adam est détectée et interprétée par la PFI de l’établissement hospitalier. La PFI analyse le contenu du courriel et transmet au destinataire la demande de traitement à réaliser sur le document contenu dans ce courriel.
Si demandé initialement, l’accusé de réception du courriel est renvoyé vers la BAL du Dr Adam Hoda suite à la réception du mail sur le serveur de messagerie de l’établissement hospitalier.


### Réception d’un compte rendu de biologie par un établissement hospitalier

**Cas d’usage :** un établissement hospitalier (le CH Martin) réceptionne, via MSSanté, un compte rendu de laboratoire concernant un patient pris en charge dans l’établissement, provenant d’un laboratoire d’analyses externe au CH Martin. Le laboratoire d’analyse ainsi que le CH Martin sont dotés d’une PFI. Ce cas d’usage nécessite un accord de partenariat entre les deux structures permettant de rendre possible l’échange MSSanté au travers des BAL applicatives.

#### Description du cas nominal

Le médecin biologiste du laboratoire d’analyses valide le compte rendu de biologie via son système de gestion de laboratoire (SGL) et précise les métadonnées de masquage du document aux PS et de visibilité au patient et à ses représentants légaux. Ces métadonnées peuvent également, selon les organisations mises en place, être paramétrées en fonction du type d’analyse réalisé. Le SGL est également paramétré pour prendre en compte les souhaits du médecin biologiste concernant la réception des accusés métier de réception DMP, de réception MSSanté par le serveur de messagerie de l’établissement CH Martin, et l’accusé métier de lecture/traitement du courriel MSSanté et du(des) document(s) CDA contenu(s) dans la pièce jointe IHE_XDM.zip.
A la validation du compte rendu de biologie par le médecin biologiste, le SGL envoie la demande d’intégration du CR de biologie dans l’application destinatrice.

La PFI du laboratoire de biologie réceptionne la demande, construit le courriel ainsi que la pièce jointe IHE_XDM.zip et l’envoi à une BAL applicative de l’établissement CH Martin dédiée ou non à la réception des CR de biologie de laboratoire partenaire. La PFI du CH Martin détecte l’arrivée du courriel, analyse son contenu et construit la demande d’intégration du CR de biologie dans le logiciel métier du destinataire (DPI).
Le DPI intègre le document à partir des informations disponibles dans la demande d’intégration et dans l’entête du document CDA, et renvoie un accusé de réception de la demande à la PFI.
Dans le contexte SEGUR vague 2, la PFI doit pouvoir générer un message MDN (Message Disposition Notification) à destination de la BAL du SGL contenant le statut de l’intégration. 
La structure du courriel MDN est décrite en annexe 4 [LIEN].


<blockquote class="stu-note">
    <p>
    <b>Point d'attention</b> dans le contexte du SEGUR vague 2, la PFI doit pouvoir générer un courriel MDN (Message Disposition Notification) à destination de la BAL du SGL contenant le statut de l'intégration.
    </p>
</blockquote>

<div class="figure">
    <img src="image8.png" alt="Figure 2" title="Figure 2 : Réception d’un CR de biologie médicale – Cas nominal" style="width:100%;">
    <figcaption>Figure 2 : Réception d’un CR de biologie médicale – Cas nominal</figcaption>
</div>
<br>
La Figure 2 illustre les échanges de bout en bout relatifs à une demande de transmission du compte rendu du SGL d’un laboratoire extérieur vers le DPI d’un établissement partenaire. 
Le diagramme serait identique dans le cas d’une demande de remplacement ou de suppression du compte rendu.

#### Description du cas en erreur

Le CR de biologie n’est pas intégré dans le logiciel métier du destinataire pour une raison technique (par exemple, non-conformité de la transaction de demande d’intégration du document) ou pour une raison fonctionnelle (par exemple, le patient n’est pas connu du logiciel destinataire).
Dans le contexte du SEGUR, la PFI doit pouvoir envoyer un accusé métier de lecture MSSanté négatif vers la BAL de l’expéditeur dans le cas où le médecin biologiste a exprimé le souhait de recevoir cet accusé de lecture MSSanté.
Sur la figure suivante, seule la partie basse de la figure précédente est représentée. Les séquences relatives à l’accusé de réception MSSanté sont identiques.


<div class="figure">
    <img src="image9.png" alt="Figure 3" title="Figure 3 : Réception d’un CR de biologie médicale – Gestion des erreurs" style="width:100%;">
    <figcaption>Figure 3 : Réception d’un CR de biologie médicale – Gestion des erreurs</figcaption>
</div>
<br>
La Figure 3 illustre la gestion des erreurs par l’établissement destinataire dans le cas d’une demande de transmission du compte rendu du SGL vers le DPI. 
Le diagramme serait identique dans le cas d’une demande de remplacement ou de suppression du compte rendu.

### Transmission d’un document clinique d’un patient d’un établissement hospitalier vers un autre établissement hospitalier

**Cas d’usage :** Le Dr Jean Dupont exerce dans le service X de l’établissement-A. Il souhaite transférer un de ses patients dans le service Y de l’établissement B. Il demande à la secrétaire médicale du service X d’envoyer le compte rendu d’hospitalisation de son patient à l’équipe de soins du service Y de l’établissement-B.
La secrétaire médicale du service X de l’établissement-A envoie un courriel à la BAL du service Y de l’établissement-B. Les deux établissements sont dotés d’une PFI.

#### Description du cas nominal

Dans ce cas d’usage, le compte rendu d’hospitalisation est envoyé par MSSanté sur la BAL organisationnelle du service Y. La secrétaire de l’établissement-B consulte sa BAL organisationnelle. Si la secrétaire souhaite intégrer automatiquement les documents de la pièce jointe IHE_XDM.zip dans le DPI, elle transfère manuellement les courriels vers la BAL applicative du service Y. Ces courriels sont ensuite détectés par la BAL applicative de la PFI de l’établissement-B qui les traitent, construit pour chaque courriel la demande d’intégration/remplacement/suppression du document et envoie cette demande au DPI du service Y. le document est intégré/remplacé/supprimé dans le DPI du service Y.
La secrétaire médicale du service X de l’établissement-A sélectionne le compte rendu et sélectionne, à partir de l’annuaire de l’établissement, la BAL organisationnelle correspondant au service Y de l’établissement-B. elle précise également si elle souhaite recevoir en retour un accusé de réception MSSanté (réception par le serveur de messagerie de l’établissement-B) ainsi qu’un accusé de lecture MSSanté (selon les organisations, ce choix peut être réalisé par paramétrage).
Cette demande d’envoi est traitée par la PFI de l’établissement-A qui réceptionne, analyse les éléments portés par la transaction émise à partir du DPI du service X et construit l’archive IHE_XDM conformément au volet Echange de documents de santé du CI_SIS en pièce jointe du courriel à destination du service Y de l’établissement-B.
Le courriel envoyé par la BAL attachée à la PFI de l’hôpital-A est réceptionné par la BAL organisationnelle du service Y. Dans le cas d’usage décrit ci-dessous, la secrétaire du service Y de l’établissement-B prend connaissance des courriels non lus dans la BAL organisationnelle du service et transfert ces courriels vers la BAL applicative du service Y dans le cas où elle désire importer automatiquement les documents dans le DPI. Si un accusé de lecture a été demandé par l’expéditeur, celui-ci est alors renvoyé vers la BAL organisationnelle du service X de l’établissement- A. Des règles peuvent également être mises en place dans le serveur de messagerie de l’établissement-B pour transférer automatiquement les courriels avec une pièce jointe IHE_XDM.zip ou un objet qui commence par XDM/1.0/DDM vers la BAL applicative du service Y.
Suite au transfert, la PFI de l’établissement-B détecte chaque courriel arrivé sur la BAL applicative du service Y. La PFI de l’hôpital-B extrait les informations du courriel ainsi que la demande d’intégration associée au document clinique et transmet ces éléments vers le DPI associé au service Y pour traitement de la demande d’intégration du document clinique dans le dossier du patient. La configuration d’une BAL applicative par service de l’établissement B permet au DPI de classer plus finement le document.
Le DPI intègre le document à partir des informations qu’il reçoit et renvoie un accusé de réception à la PFI. 
Dans le contexte du SEGUR vague 2, la PFI doit pouvoir générer un message MDN (Message Disposition Notification) à destination de la BAL organisationnelle du service Y contenant le statut de l’intégration du document. En cas d’erreur, la secrétaire pourra envisager une intégration manuelle (voir le paragraphe suivant). 
La structure du message MDN est précisée en annexe 4 [LIEN].

<blockquote class="stu-note">
    <p>
    <b>Point d'attention</b> ce cas d’usage décrit un mécanisme de traitement d’un courriel réceptionné sur une BAL organisationnelle. Ce mécanisme pourrait être identique pour un courriel réceptionné sur une BAL personnelle, sous réserve de s’assurer et de respecter les exigences réglementaires relatives au transfert d’un courriel personnel dans un contexte professionnel.
    </p>
</blockquote>

Ce cas d’usage nécessite de définir une BAL organisationnelle ainsi qu’une BAL applicative associée pour chaque service clinique de l’établissement B. La PFI ou le DPI peuvent prévoir un paramétrage pour associer un service clinique de l’établissement à une BAL afin de classer les documents dans le bon service.


<div class="figure">
    <img src="image10.png" alt="Figure 4" title="Figure 4 : Transmission d’un document clinique d’un patient d’un CH vers un autre CH -Cas nominal" style="width:100%;">
</div>
<div class="figure">
    <img src="image11.png" alt="Figure 4" title="Figure 4 : Transmission d’un document clinique d’un patient d’un CH vers un autre CH -Cas nominal" style="width:100%;">
    <figcaption>Figure 4 : Transmission d’un document clinique d’un patient d’un CH vers un autre CH -Cas nominal</figcaption>
</div>    
<br>

La Figure 4 illustre les échanges de bout en bout relatifs à une demande de transmission du compte rendu du SGL vers le DPI.
Le diagramme serait identique dans le cas d’une demande de remplacement ou de suppression du compte rendu.

#### Description du cas d'usage en erreur

La cinématique des échanges est la même que précédemment mais le compte rendu d’hospitalisation n’est pas intégré dans le DPI du service Y en raison de l’inexistence du patient dans le DPI.
La figure ci-dessous représente uniquement la partie basse de la figure précédente, à partir de la lecture par la PFI de la BAL applicative de l’établissement-B.


<div class="figure">
    <img src="image12.png" alt="Figure 5" title="Figure 5 : Transmission d’un document clinique d’un patient d’un CH vers un autre CH -Gestion des erreurs" style="width:100%;">
    <figcaption>Figure 5 : Transmission d’un document clinique d’un patient d’un CH vers un autre CH -Gestion des erreurs</figcaption>
</div>    
<br>


La Figure 5 illustre la gestion des erreurs par l’établissement destinataire dans le cas d’une demande de transmission d’un compte rendu vers le DPI d’un autre établissement. 
Le diagramme serait identique dans le cas d’une demande de remplacement ou de suppression du compte rendu.
