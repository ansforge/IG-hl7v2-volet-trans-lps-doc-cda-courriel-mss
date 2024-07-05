Les échanges sont représentés de bout en bout pour permettre au lecteur
d'avoir une vision de l'ensemble des échanges, y compris du côté du
destinataire. Cependant, le périmètre du présent volet est limité aux
transactions représentées en bleu sur les figures suivantes.

### Implémentation du message ORU et de ses acquittements métier HL7

<div class="figure">
    <img src="image17.png" alt="Figure 13" title="Figure 13 : Diagramme de séquence -- Message ORU" style="width:100%;">
</div>
<div class="figure">
    <img src="image18.png" alt="Figure 13">
    <figcaption>Figure 13 : Diagramme de séquence -- Message ORU</figcaption>
</div>
<br>

Les interactions de la transaction de
transmission/remplacement/suppression de document(s) utilisent le
message HL7 ORU\^R01\^ORU_R01 en version 2.5 ainsi que ses acquittements
métiers HL7 ZAM\^Z01\^ZAM_Z01 (accusé métier de réception DMP),
ZAM\^Z02\^ZAM_Z01 (accusé métier de réception MSSanté) et
ZAM_Z03\^ZAM_Z01 (accusé métier de lecture MSSanté).

L'action à réaliser sur le document porté par la transaction est
indiquée par la valeur renseignée au niveau du champ OBX-11 du segment
OBX portant le document (cf section 12.2.6 LIEN), qui prend la valeur F (pour
demande d'intégration du document), C (pour demande de remplacement de
document) et D (pour demande de suppression de document), et sur la
valeur du champ ORC-1 (cf section 12.2.4 LIEN).

Pour des questions de lisibilité, la figure 13 représente sur le même
schéma la possibilité pour l'acteur CREATEUR d'envoyer une demande
d'intégration, de remplacement ou de suppression de document(s) au moyen
d'un message HL7 ORU.

### Implémentation du message MDM et de ses acquittements métier HL7

Les interactions de la transaction de
transmission/remplacement/suppression de document(s) utilisent
respectivement les messages HL7 MDM\^T02\^MDM_T02, MDM\^T10\^MDM_T10 et
MDM\^T04\^MDM_T04 en version 2.6 ainsi que ses acquittements métiers HL7
ZAM\^Z01\^ZAM_Z01 (accusé métier de réception DMP), ZAM\^Z02\^ZAM_Z01
(accusé métier de réception MSSanté) et ZAM_Z03\^ZAM_Z01 (accusé métier
de lecture MSSanté).

L'action à réaliser sur le document porté par la transaction est
indiquée par la nature de l'événement (T02, T10 et T04).

#### Demande de transmission initiale d'un document

<div class="figure">
    <img src="image19.png" alt="Figure 14" title="Figure 14 : Diagramme de séquence -- Message MDM -- Transmission initiale d'un document" style="width:100%;">
</div>
<div class="figure">
    <img src="image18.png" alt="Figure 14">
    <figcaption>Figure 14 : Diagramme de séquence -- Message MDM -- Transmission initiale d'un document</figcaption>
</div>
<br>

#### Demande de remplacement d'un document


<div class="figure">
    <img src="image20.png" alt="Figure 15" title="Figure 15 : Diagramme de séquence -- Message MDM -- Remplacement d'un document" style="width:100%;">
</div>
<div class="figure">
    <img src="image18.png" alt="Figure 15">
    <figcaption>Figure 15 : Diagramme de séquence -- Message MDM -- Remplacement d'un document</figcaption>
</div>
<br>

#### Demande de suppression d'un document


<div class="figure">
    <img src="image21.png" alt="Figure 16" title="Figure 16 : Diagramme de séquence -- Message MDM -- Suppression de document(s)" style="width:100%;">
</div>
<div class="figure">
    <img src="image18.png" alt="Figure 16">
    <figcaption>Figure 16 : Diagramme de séquence -- Message MDM -- Suppression de document(s)</figcaption>
</div>
<br>