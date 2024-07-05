Cette section décrit, à titre d'exemple et de façon non exhaustive, un ensemble de cas d'usage. Pour une meilleure compréhension du lecteur, ces cas d'usage couvrent les échanges entre le système créateur du document et la PFI, mais également les échanges au-delà de la PFI (et donc au-delà du périmètre de ce présent document).

### Envoi d'un document clinique d'un établissement vers un médecin traitant

<blockquote>
    <div class="note note">
    <u>Cas d'usage :</u> un médecin d'un établissement publie sur le DMP un document clinique concernant un patient et envoi par MSSanté même document au médecin traitant du patient.
    </div>
</blockquote>

Le Dr Jean Dupont exerçant à l'hôpital-A (<jean.dupont@hopital-A.mssante.fr> ) créé un compte rendu pour son patient au cours d'une consultation externe dans l'établissement. Il souhaite publier sur le DMP ce compte rendu à partir de son application métier et souhaite en même temps l'adresser par MSSanté au médecin traitant du patient, le Dr Adam Hoda (<adam.hoda@medecin.mssante.fr>).

Le Dr Dupont (hôpital-A) sélectionne ce compte rendu dans son
application métier, il précise les métadonnées de masquage du document
aux PS et de visibilité au patient et à ses représentants légaux. Il
précise également au travers de l'IHM de son application métier qu'il
souhaite publier ce compte rendu sur le DMP du patient et envoyer ce
compte rendu au Dr Adam Hoda en sélectionnant dans son annuaire
l'adresse e-mail de ce médecin traitant. Avant de valider sa demande, le
Dr Dupont peut préciser s'il souhaite recevoir un accusé de réception
DMP, un accusé de réception MSSanté et un accusé de lecture du courriel
par le Dr Adam Hoda.

La demande du Dr Dupont est traitée par le composant PFI de l'hôpital-A
qui gère les échanges avec le DMP et/ou la MSSanté. La PFI de
l'hôpital-A réceptionne et analyse les éléments portés par la
transaction émise à partir du logiciel métier du Dr Dupont. La PFI
construit d'une part la requête d'alimentation du DMP conformément au
*Guide d'implémentation du DMP* ainsi que le courriel à destination de
la BAL personnelle du Dr Adam Hoda. La PFI construit également les
pièces jointes, c'est-à-dire l'archive IHE_XDM.zip conformément au volet
*Echange de documents de santé* du CI_SIS et les fichiers PDF
correspondants aux comptes rendus envoyés dans l'archive IHE_XDM.

Si demandé initialement, le logiciel métier du Dr Dupont réceptionne en
retour, via la PFI, l'accusé métier d'intégration au DMP ainsi que
l'accusé métier de réception du courriel MSSanté provenant du serveur de
messagerie du Dr Adam Hoda. Dans le cas où le Dr Dupont a également
demandé un accusé métier de lecture lors de l'envoi par MSSanté,
celui-ci est notifié, dans son logiciel métier, de la prise de
connaissance du courriel par le Dr Adam Hoda.

### Envoi d'un compte rendu de biologie d'un laboratoire privé vers un établissement hospitalier

<blockquote>
    <div class="note note">
    <u>Cas d'usage :</u> un établissement hospitalier (le CH Martin) réceptionne, via MSSanté, un compte rendu de laboratoire concernant un patient pris en charge dans l'établissement, provenant d'un laboratoire d'analyses externe au CH Martin. Le laboratoire d'analyse ainsi que le CH Martin sont dotés de PFI qui gèrent l'échange de courriel entre la BAL applicative du laboratoire et la BAL applicative du DPI de l'établissement consommateur.
    </div>
</blockquote>

<blockquote class="stu-note">
    <p>
    <b>Point d'attention</b> ce cas d'usage nécessite un accord de partenariat entre les deux structures permettant de rendre possible l'échange MSSanté au travers des BAL applicatives.
    </p>
</blockquote>

Ce cas d'usage peut être étendu à tout échange entre 2 boîtes applicatives. Ce processus est similaire à l'envoi d'un document via un
message HL7, mais le vecteur de communication est un courriel MSSanté.

#### Description du cas nominal

Le médecin biologiste valide le compte rendu de biologie via son SGL
(Système de Gestion de Laboratoire) et précise les métadonnées de
masquage du document aux PS et de visibilité au patient et à ses
représentants légaux. Ces attributs peuvent également, selon les
organisations mises en place, être paramétrées en fonction du type
d'analyse réalisé. Le SGL est également paramétré pour prendre en compte
les souhaits du médecin biologiste concernant la réception des accusés
métier de réception DMP, de réception du courriel MSSanté par le serveur
de messagerie de l'établissement CH Martin et de lecture/traitement du
courriel MSSanté et du(des) document(s) CDA contenu(s) dans la pièce
jointe IHE_XDM.zip.

A la validation du compte rendu de biologie par le médecin biologiste,
le SGL envoie la demande d'intégration du CR de biologie dans
l'application destinatrice.

La PFI du laboratoire de biologie réceptionne la demande, construit le
courriel et la pièce jointe IHE_XDM.zip et l'envoie à une BAL
applicative de l'établissement CH Martin dédiée ou non à la réception
des CR de biologie de laboratoire partenaire. La PFI du CH Martin
détecte l'arrivée du courriel, analyse son contenu et construit la
demande d'intégration du CR de biologie dans le logiciel métier du
destinataire (DPI).

Le DPI intègre le document à partir des informations disponibles dans la
demande d'intégration du document et de l'entête du document CDA, et
renvoie un accusé de réception de la demande à la PFI.


<blockquote class="stu-note">
    <p>
    <b>Point d'attention</b> dans le contexte du SEGUR vague 2, la PFI doit pouvoir générer un courriel MDN (Message Disposition Notification) à destination de la BAL du SGL contenant le statut de l'intégration.
    </p>
</blockquote>

La structure du message MDN est décrite dans l'exemple accessible [ici](exemples.html).


<div class="figure">
    <img src="image6.png" alt="Figure 2" title="Figure 2 : Envoi d'un CR de biologie médicale -- Cas nominal" style="width:100%;">
    <figcaption>Figure 2 : Envoi d'un CR de biologie médicale -- Cas nominal</figcaption>
</div>
<br>
La Figure 2 illustre les échanges de bout en bout relatifs à une demande
de transmission du compte rendu du SGL d'un laboratoire extérieur vers
le DPI d'un établissement partenaire.

Le diagramme serait identique dans le cas d'une demande de remplacement
ou de suppression du compte rendu.

#### Description du cas en erreur

Le CR de biologie n'est pas intégré dans le logiciel métier du
destinataire pour une raison technique (par exemple, non-conformité de
la transaction de demande d'intégration du document) ou pour une raison
fonctionnelle (par exemple, le patient n'est pas connu du logiciel
destinataire).

Dans le contexte du SEGUR vague 2, la PFI du CH Martin doit pouvoir
envoyer un accusé métier de lecture/traitement MSSanté négatif vers la
BAL de l'expéditeur dans le cas où le médecin biologiste a exprimé le
souhait de recevoir cet accusé de lecture MSSanté.

Sur la figure suivante, seule la partie basse de la figure précédente
est représentée. Les séquences relatives à l'accusé de réception MSSanté
sont identiques.

<div class="figure">
    <img src="image7.png" alt="Figure 3" title="Figure 3 : Envoi d'un CR de biologie médicale -- Gestion des erreurs" style="width:100%;">
    <figcaption>Figure 3 : Envoi d'un CR de biologie médicale -- Gestion des erreurs</figcaption>
</div>
<br>
La Figure 3 illustre la gestion des erreurs par l'établissement
destinataire dans le cas d'une demande de transmission du compte rendu
du SGL vers le DPI.

Le diagramme serait identique dans le cas d'une demande de remplacement
ou de suppression du compte rendu.

### Transmission d'un document clinique d'un patient d'un établissement hospitalier vers un autre établissement hospitalier

<blockquote>
    <div class="note note">
    <u>Cas d'usage :</u> Le Dr Jean Dupont exerce dans le service X de l'établissement A. Il souhaite transférer un de ses patients dans le service Y de l'établissement B. Il demande à la secrétaire médicale du service X d'envoyer le compte rendu d'hospitalisation de son patient à l'équipe de soins du service Y de l'établissement B.
    <br>
    La secrétaire médicale du service X de l'établissement A envoie un courriel à la BAL du service Y de l'établissement B. Les deux établissements sont dotés d'une PFI.
    </div>
</blockquote>


#### Description du cas nominal

Dans ce cas d'usage, le compte rendu d'hospitalisation est envoyé par
MSSanté sur la BAL organisationnelle du service Y. La secrétaire de
l'établissement B consulte sa BAL organisationnelle. Si la secrétaire
veut intégrer les documents de la pièce jointe IHE_XDM.zip dans le DPI,
elle transfère manuellement les courriels vers la BAL applicative du
service Y. Ces courriels sont ensuite détectés par la BAL applicative de
la PFI de l'établissement B qui les traitent, construit pour chaque
courriel la demande d'intégration/remplacement/suppression du document
et envoie cette demande au DPI du service Y. le document est
intégré/remplacé/supprimé dans le DPI du service Y.

La secrétaire médicale du service X de l'établissement-A sélectionne le
compte rendu et sélectionne à partir de l'annuaire de l'établissement la
BAL organisationnelle correspondant au service Y de l'établissement B.
elle précise également si elle souhaite recevoir en retour un accusé de
réception MSSanté (réception par le serveur de messagerie de
l'établissement B) ainsi qu'un accusé de lecture MSSanté (selon les
organisations, ce choix peut être réalisé par paramétrage).

Cette demande d'envoi est traitée par la PFI de l'établissement-A qui
réceptionne, analyse les éléments portés par la demande de traitement
émise à partir du DPI du service X et construit l'archive IHE_XDM
conformément au volet *Echange de documents de santé* du CI_SIS en pièce
jointe du courriel à destination du service Y de l'établissement-B. La
PFI attache également la version PDF correspondant à chaque document
CDA.

Le courriel envoyé par la BAL attachée à la PFI de l'établissement-A est
réceptionné par la BAL organisationnelle du service Y de
l'établissement-B. Dans le cas d'usage décrit ci-dessous, la secrétaire
du service Y de l'établissement B prend connaissance des courriels non
lus dans la BAL organisationnelle du service Y et transfert ces
courriels vers la BAL applicative du service Y dans le cas où elle
désire importer automatiquement les documents dans le DPI. Si un accusé
de lecture a été demandé par l'expéditeur, celui-ci est alors renvoyé
vers la BAL organisationnelle du service X de l'établissement-A. Des
règles peuvent également être mises en place dans le serveur de
messagerie de l'établissement-B pour transférer automatiquement les
courriels avec une pièce jointe IHE_XDM.zip ou un objet qui commence par
XDM/1.0/DDM vers la BAL applicative du service Y.

Suite au transfert, la BAL de la PFI de l'établissement-B détecte chaque
courriel arrivé sur la BAL applicative du service Y. La PFI extrait les
informations du courriel ainsi que la demande d'intégration associée au
document clinique et transmet ces éléments vers le DPI associé au
service Y pour traitement de la demande d'intégration du document
clinique dans le dossier du patient. La configuration d'une BAL
applicative par service de l'établissement-B permet au DPI de classer
plus finement le document.

Le DPI intègre le document à partir des informations qu'il reçoit et
renvoie un accusé de réception de la demande de traitement à la PFI de
l'établissement-B. La PFI doit pouvoir générer un message MDN (Message
Disposition Notification) à destination de la BAL de service Y contenant
le statut de l'intégration du document. En cas d'erreur, la secrétaire
pourra envisager une intégration manuelle (voir le paragraphe suivant).

La structure du message MDN est décrite dans l'exemple accessible [ici](exemples.html).

La figure ci-dessous illustre ce cas d'usage.

<blockquote class="stu-note">
    <p>
    <b>Point d'attention</b> ce cas d'usage décrit un mécanisme de traitement d'un courriel réceptionné sur une BAL organisationnelle. Ce mécanisme pourrait être identique pour un courriel réceptionné sur une BAL personnelle, sous réserve de respecter les exigences réglementaires relatives au transfert d'un courriel personnel dans un contexte professionnel.
    Ce cas d'usage nécessite de définir une BAL organisationnelle ainsi qu'une BAL applicative associée pour chaque service clinique de l'établissement B. La PFI ou le DPI peuvent prévoir un paramétrage pour associer un service clinique de l'établissement à une BAL afin de classer les documents dans le bon service.
    </p>
</blockquote>


<div class="figure">
    <img src="image8.png" alt="Figure 4" title="Figure 4 : Transmission d'un document clinique d'un patient d'un CH vers un autre CH -Cas nominal" style="width:100%;">
</div>
<div class="figure">
    <img src="image9.png" alt="Figure 4" title="Figure 4 : Transmission d'un document clinique d'un patient d'un CH vers un autre CH -Cas nominal" style="width:100%;">
    <figcaption>Figure 4 : Transmission d'un document clinique d'un patient d'un CH versun autre CH -Cas nominal</figcaption>
</div>    
<br>

La Figure 4 illustre les échanges de bout en bout relatifs à une demande
de transmission du compte rendu du SGL vers le DPI.

Le diagramme serait identique dans le cas d'une demande de remplacement
ou de suppression du compte rendu.

#### Description du cas d'usage en erreur

La cinématique des échanges est la même que précédemment mais le compte
rendu d'hospitalisation n'est pas intégré dans le DPI du service Y en
raison, par exemple, de l'inexistence du patient dans le DPI.

La figure ci-dessous représente uniquement la partie basse de la figure
précédente, à partir du transfert du courriel avec pièce jointe vers la
BAL applicative de l'établissement-B.

<div class="figure">
    <img src="image10.png" alt="Figure 5" title="Figure 5 : Transmission d'un document clinique d'un patient d'un CH vers un autre CH -Gestion des erreurs" style="width:100%;">
    <figcaption>Figure 5 : Transmission d'un document clinique d'un patient d'un CH vers un autre CH -Gestion des erreurs</figcaption>
</div>    
<br>



La Figure 5 illustre la gestion des erreurs par l'établissement
destinataire dans le cas d'une demande de transmission d'un compte rendu
vers le DPI d'un autre établissement.

Le diagramme serait identique dans le cas d'une demande de remplacement
ou de suppression du compte rendu.