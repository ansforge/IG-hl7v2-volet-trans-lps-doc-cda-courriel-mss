#### Le message MDM en HL7 v2.6

##### Description du profil du message MDM
Le profil du message MDM est le suivant :
<table class="table-hl7v2">
  <tr>
    <th>
      <p>Segment</p>
    </th>
    <th>
      <p>Meaning</p>
    </th>
    <th>
      <p>Usage</p>
    </th>
    <th>
      <p>Card.</p>
    </th>
    <th>
      <p>§ HL7</p>
    </th>
  </tr>
  <tbody>
    <tr>
      <td>
        <p>MSH</p>
      </td>
      <td>
        <p>Message Header</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p>2</p>
      </td>
    </tr>
    <tr>
      <td>
        <p> [{SFT}]</p>
      </td>
      <td>
        <p>Software Segment</p>
      </td>
      <td>
        <p>O</p>
      </td>
      <td>
        <p>[0..*]</p>
      </td>
      <td>
        <p>2</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>[UAC]</p>
      </td>
      <td>
        <p>User Authentication Credentials</p>
      </td>
      <td>
        <p>O</p>
      </td>
      <td>
        <p>[0..1]</p>
      </td>
      <td>
        <p>2</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>EVN</p>
      </td>
      <td>
        <p>Event type</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p>2</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PID</p>
      </td>
      <td>
        <p>Patient Identification</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p>3</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PV1</p>
      </td>
      <td>
        <p>Patient Visit</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p>3</p>
      </td>
    </tr>
    <tr>
      <td>
        <p> </p>
      </td>
      <td>
        <p>--- COMMON_ORDER begin</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p> ORC</p>
      </td>
      <td>
        <p>Common Order = demande de service sur le document</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p>4</p>
      </td>
    </tr>
    <tr>
      <td>
        <p> [{</p>
      </td>
      <td>
        <p>--- TIMING begin</p>
      </td>
      <td>
        <p>O</p>
      </td>
      <td>
        <p>[0..*]</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>  TQ1</p>
      </td>
      <td>
        <p>Timing/Quantity</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p>4</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>  [{TQ2}]</p>
      </td>
      <td>
        <p>Timing/Quantity RelationShip</p>
      </td>
      <td>
        <p>O</p>
      </td>
      <td>
        <p>[0..*]</p>
      </td>
      <td>
        <p>4</p>
      </td>
    </tr>
    <tr>
      <td>
        <p> }]</p>
      </td>
      <td>
        <p>--- TIMING end</p>
      </td>
      <td>
        <p> </p>
      </td>
      <td>
        <p> </p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p> OBR</p>
      </td>
      <td>
        <p>Observation Request segment</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p>4</p>
      </td>
    </tr>
    <tr>
      <td>
        <p> [{NTE}]</p>
      </td>
      <td>
        <p>Notes and comments</p>
      </td>
      <td>
        <p>O</p>
      </td>
      <td>
        <p>[0..*]</p>
      </td>
      <td>
        <p>2</p>
      </td>
    </tr>
    <tr>
      <td>
        <p> </p>
      </td>
      <td>
        <p>--- COMMON_ORDER end</p>
      </td>
      <td>
        <p> </p>
      </td>
      <td>
        <p> </p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>TXA</p>
      </td>
      <td>
        <p>Transcription document header</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p>9</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>{</p>
      </td>
      <td>
        <p>OBXNTE (Document, informations sur le courriel, métadonnées sur le document)</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..*]</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p> OBX</p>
      </td>
      <td>
        <p>Observation/Result</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p>9</p>
      </td>
    </tr>
    <tr>
      <td>
        <p> [{PRT}]</p>
      </td>
      <td>
        <p>Participation : Expéditeur, destinataire(s) MSS et adresse mail sur laquelle le destinataire peut répondre. Segment PRT pré-adopté de la version 2.9</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..*]</p>
      </td>
      <td>
        <p>7 (v2.9)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p> [{NTE}]</p>
      </td>
      <td>
        <p>Notes and comments</p>
      </td>
      <td>
        <p>O</p>
      </td>
      <td>
        <p>[0..*]</p>
      </td>
      <td>
        <p>2</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>}</p>
      </td>
      <td>
        <p>---OBXNTE end</p>
      </td>
      <td>
        <p> </p>
      </td>
      <td>
        <p> </p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
  </tbody>
</table>

Le message HL7 MDM ne peut transmettre qu’un seul document médical.

Les contraintes apportées par ce volet sur les données du message MDM sont décrites à la [section dédiée](volume2.html#contraintes-appliquées-aux-messages-mdm-dans-le-contexte-de-ce-volet).

##### Description fonctionnelle du message MDM

<div class="figure" style='text-align: center;'>
    <img src="image20.png" alt="Figure 14" title="Figure 14 : Description fonctionnelle du message HL7 MDM" style="width:80%;">
    <figcaption><b>Figure 14 : Description fonctionnelle du message HL7 MDM</b></figcaption>
</div>    
<br>
Les groupes de segments en rouge sur le schéma représentent les éléments
spécifiques à ce volet :

-   Un groupe OBXNTE, requis, contenant le document médical au format
    CDA-R2 codé en base64 suivi de segments PRT, pré-adoptés depuis la
    version 2.9 du standard, permettant ainsi de renseigner les
    informations de l'expéditeur (requis), le destinataire MSSanté
    (requis si connu) et, le cas échéant, l'adresse mail de réponse
    (contraintes décrites au [paragraphe dédié](volume2.html#le-groupe-de-segments-obxnte-portant-le-document-cda)).

-   Le deuxième groupe véhicule, dans un segment OBX, les informations
    du courriel MSSanté dont a été extrait le document.

-   Les groupes OBXNTE suivants (requis et répétables) véhiculent les
    métadonnées spécifiques à l'envoi par la MSSanté.

Dans le message MDM, le document est accompagné de quelques métadonnées
renseignées au niveau du segment TXA. Il s'agit à minima du type de
document (TXA-2), de la présentation du contenu du document (TXA-3), de
l'identifiant unique du document (TXA-12), de l'identifiant unique du
document remplacé (TXA-13) lorsque l'évènement est à T10 et du statut
indiquant la complétude du document (TXA-17).

#### Contraintes appliquées aux messages MDM dans le contexte de ce volet
Dans la suite de cette section, les valeurs indiquées en bleu dans les tableaux indiquent les valeurs fixes à insérer dans le champ du message.

##### Eléments de contrôle du message MDM

###### Le segment MSH – Header du message

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th>
        <p>Champ</p>
      </th>
      <th>
        <p>Contenu</p>
      </th>
      <th>
        <p>Type donnée</p>
      </th>
      <th>
        <p>Caractère optionnel/obligatoire</p>
        <p> </p>
        <p> </p>
      </th>
    </tr>
    <tr>
      <td>
        <p>MSH-1</p>
      </td>
      <td>
        <p><span class="hl7-color">|</span> séparateur de champ</p>
      </td>
      <td>
        <p>ST</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-2</p>
      </td>
      <td>
        <p><span class="hl7-color">^~\&</span> : séparateur de composant, répétition, caractère d'échappement, séparateur de sous-composants</p>
      </td>
      <td>
        <p>ST</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-3</p>
      </td>
      <td>
        <p>Application émettrice</p>
      </td>
      <td>
        <p>HD</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-4</p>
      </td>
      <td>
        <p>Organisation émettrice</p>
      </td>
      <td>
        <p>HD</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-5</p>
      </td>
      <td>
        <p>Application réceptrice</p>
      </td>
      <td>
        <p>HD</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-6</p>
      </td>
      <td>
        <p>Organisation réceptrice</p>
      </td>
      <td>
        <p>HD</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-7</p>
      </td>
      <td>
        <p>Date/time du message</p>
      </td>
      <td>
        <p>TS</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-9</p>
      </td>
      <td>
        <p>Type du message</p>
        <p><span class="hl7-color">MDM^T02^MDM_T02</span></p>
        <p><span class="hl7-color">MDM^T10^MDM_T02</span></p>
        <p><span class="hl7-color">MDM^T04^MDM_T02</span></p>
      </td>
      <td>
        <p>MSG</p>
      </td>
      <td>
        <p>R</p>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-10</p>
      </td>
      <td>
        <p>Identifiant du message</p>
      </td>
      <td>
        <p>ST</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-11</p>
      </td>
      <td>
        <p>Processing Id</p>
        <p><span class="hl7-color">P : en production</span></p>
        <p><span class="hl7-color">T : message de test</span></p>
        <p><span class="hl7-color">D : environnement de debug</span></p>
      </td>
      <td>
        <p>PT</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-12</p>
      </td>
      <td>
        <p>Version du standard <span class="hl7-color">2.6</span></p>
      </td>
      <td>
        <p>VID</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-17</p>
      </td>
      <td>
        <p><span class="hl7-color">FRA</span></p>
      </td>
      <td>
        <p>ID</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-18</p>
      </td>
      <td>
        <p>Jeux de caractères, valeurs possibles :</p>
        <p><span class="hl7-color">UNICODE UTF-8</span> ou <span class="hl7-color">8859/15</span></p>
      </td>
      <td>
        <p>ID</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-21</p>
      </td>
      <td>
        <p>Identifiant du profil de message</p>
        <p>MSH-21.1 : Entity Identifier (<span class="hl7-color">1.1</span>)</p>
        <p>MSH-21.2 : Namespace Id</p>
        <p><span class="hl7-color">CISIS_CDA_HL7_LPS</span></p>
      </td>
      <td>
        <p>EI</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
  </tbody>
</table>

###### Exemples

Entête MSH d’un message MDM émis par le GESTIONNAIRE :

`MSH|^~\&|PFI|CHU_X|DPI|CHU_X|202310030830||MDM^T02^MDM^T02^MDM_T02|12345|P|2.6|||||FRA|8859/15|||1.1^ CISIS_CDA_HL7_LPS`

##### Les données concernant le patient et la venue du patient

Le message HL7 MDM est centré sur un seul patient. Les informations concernant le patient sont décrites par le segment requis PID. Le segment PV1, requis dans le standard, représente la venue courante du patient.

Ces deux segments doivent être renseignés conformément à la spécification « [PAM – National extension France » version 2.11](https://www.interopsante.org/publications) publiée en 2024. Si l’INS est véhiculé, le segment PID doit suivre les contraintes décrites dans l’[annexe CI-SIS « Prise en charge de l’identifiant National de Santé (INS) dans les standards d’interopérabilité et les volets du CI-SIS »](https://esante.gouv.fr/annexe-prise-en-charge-de-lins-dans-les-volets-du-ci-sis).

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th>
        <p>Champ</p>
      </th>
      <th>
        <p>Contenu</p>
      </th>
      <th>
        <p>Type donnée</p>
      </th>
      <th>
        <p>Caractère optionnel/obligatoire</p>
      </th>
    </tr>
    <tr>
      <td>
        <p>PID-3</p>
      </td>
      <td>
        <p>Identifiants du patient</p>
      </td>
      <td>
        <p>CX</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PID-5</p>
      </td>
      <td>
        <p>Nom du patient</p>
      </td>
      <td>
        <p>XPN</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
  </tbody>
</table>

Le PID-3 doit être identique aux identifiants de patient portés par le document CDA (recordTarget/patientRole/id).

Pour le segment PV1, ce volet ajoute les contraintes suivantes :
<table class="table-hl7v2">
  <tbody>
    <tr>
      <th>
        <p>Champ</p>
      </th>
      <th>
        <p>Contenu</p>
      </th>
      <th>
        <p>Type donnée</p>
      </th>
      <th>
        <p>Caractère optionnel/obligatoire</p>
      </th>
    </tr>
    <tr>
      <td>
        <p>PV1-2</p>
      </td>
      <td>
        <p>Classe du patient : <span class="hl7-color">N</span> (Not applicable)</p>
      </td>
      <td>
        <p>IS</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
  </tbody>
</table>

##### Le segment ORC

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th colspan="3">
        <p>Composition du segment ORC : Usage = Required / Cardinalité = [1..1]</p>
      </th>
    </tr>
    <tr>
      <th>
        <p>Elément requis :</p>
      </th>
      <th>
        <p>Description :</p>
      </th>
      <th>
        <p>Valeur :</p>
      </th>
    </tr>
    <tr>
      <td>
        <p><strong>Segment ORC</strong></p>
      </td>
      <td>
        <p><strong>Common Order</strong></p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>ORC-1</p>
      </td>
      <td>
        <p>Order control</p>
      </td>
      <td>
        <p><span class="hl7-color">NW</span> (New order/service dans le cas d'une demande d'intégration de document(s)</p>
        <p><span class="hl7-color">RO</span> (Replace order) dans le cas d'une demande de remplacement</p>
        <p><span class="hl7-color">CA</span> (Canceled) dans le cas d'une demande de suppression</p>
      </td>
    </tr>
  </tbody>
</table>

##### Le segment OBR

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th colspan="3">
        <p>Composition du segment OBR : Usage = Required / Cardinalité = [1..1]</p>
      </th>
    </tr>
    <tr>
      <th>
        <p>Elément requis :</p>
      </th>
      <th>
        <p>Description :</p>
      </th>
      <th>
        <p>Valeur :</p>
      </th>
    </tr>
    <tr>
      <td>
        <p><strong>Segment OBR</strong></p>
      </td>
      <td>
        <p><strong>Observation Request</strong></p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBR-4</p>
      </td>
      <td>
        <p>Universal Service Identifier</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt;OBR-4.1</p>
      </td>
      <td>
        <p>Code du document</p>
      </td>
      <td rowspan="2">
        <p>Utiliser le <a href="https://ansforge.github.io/IG-terminologie-de-sante/ig/main/ValueSet-JDV-J07-XdsTypeCode-CISIS.html">JDV_J07-XdsTypeCode-CISIS</a> de la Nomenclature des Objets de Santé (NOS).</p>
        <p>A noter qu'en cas d'envoi au DMP, le Gestionnaire doit contrôler que le type de document appartient au jeu de valeur défini par le DMP (<a href="https://ansforge.github.io/IG-terminologie-de-sante/ig/main/ValueSet-JDV-J66-TypeCode-DMP.html">JDV_J66-TypeCode-DMP</a>).</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt;OBR-4.2</p>
      </td>
      <td>
        <p>Libellé du document</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt;OBR-4.3</p>
      </td>
      <td>
        <p>Système de codage dont est issu le code</p>
      </td>
      <td>
        <p><span class="hl7-color">LN</span> ou <span class="hl7-color">TRE_A05</span><a href="https://ansforge.github.io/IG-terminologie-de-sante/ig/main/CodeSystem-TRE-A05-TypeDocComplementaire.html"> (lien vers la TRE)</a> en fonction de l'appartenance du code à l'un des trois systèmes de codage</p>
      </td>
    </tr>
  </tbody>
</table>

##### Les données d’entête du document – Segment TXA

Le message MDM requiert l’utilisation du segment TXA qui porte les métadonnées associées au document contenu dans le message. Les contraintes apportées par ce volet sur le segment TXA sont les suivantes :
<table class="table-hl7v2">
  <tbody>
    <tr>
      <th>
        <p>Champ</p>
      </th>
      <th>
        <p>Contenu</p>
      </th>
      <th>
        <p>Type donnée</p>
      </th>
      <th>
        <p>Caractère optionnel/obligatoire</p>
      </th>
    </tr>
    <tr>
      <td>
        <p>TXA-1</p>
      </td>
      <td>
        <p>Set-ID TXA. Valeur = 1</p>
      </td>
      <td>
        <p>SI</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>TXA-2</p>
      </td>
      <td>
        <p>Type de document dont les valeurs sont à prendre dans</p>
        <p>le <a href="https://ansforge.github.io/IG-terminologie-de-sante/ig/main/ValueSet-JDV-J07-XdsTypeCode-CISIS.html">JDV_J07-XdsTypeCode-CISIS</a> de la Nomenclature des Objets de Santé (NOS).</p>
        <p>Par exemple : 11502-2</p>
      </td>
      <td>
        <p>IS</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>TXA-3</p>
      </td>
      <td>
        <p>Document Content Presentation</p>
        <p><span class="hl7-color">TEXT</span></p>
      </td>
      <td>
        <p>ID</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>TXA-12 <i>(Note 1)</i></p>
      </td>
      <td>
        <p>Unique document number</p>
        <p>Si ClinicalDocument/id@extension est renseigné :</p>
        <p> ex : 58132^^1.2.250.2345.3245.13^ISO</p>
        <p>Si ClinicalDocument/id@extension n'est pas renseigné :</p>
        <p> ex : 1.2.250.2345.3245.13.58132</p>
      </td>
      <td>
        <p>EI</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>TXA-13 <i>(Note 1)</i></p>
      </td>
      <td>
        <p>Parent document number</p>
        <p>Si ClinicalDocument/id@extension est renseigné :</p>
        <p> ex : 58131^^1.2.250.2345.3245.13^ISO</p>
        <p>Si ClinicalDocument/id@extension n'est pas renseigné :</p>
        <p> ex : 1.2.250.2345.3245.13.58131</p>
      </td>
      <td>
        <p>EI</p>
      </td>
      <td>
        <p>C (Requis dans le cas d'une demande de remplacement)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>TXA-17</p>
      </td>
      <td>
        <p>Document completion status dont la valeur est à prendre dans la table HL7 0271</p>
        <p><span class="hl7-color">AU</span></p>
      </td>
      <td>
        <p>ID</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
  </tbody>
</table>

**(Note 1)** : _conformément au volet de **Structuration minimale des
documents de santé**, l'identifiant du document au sein du document CDA
s'exprime soit par un OID complet identifiant complètement l'instance du
document (sans extension), soit par une racine d'OID commune à toutes
les instances de documents de l'émetteur associée à une extension propre
à l'instance du document._

La règle de peuplement des sous champs des champs TXA-12 et TXA-13 est
la suivante :

-   si ClinicalDocument/id@extension est renseigné :

    -   TXA-12.1 < = ClinicalDocument/id@extension

    -   TXA-12.2 < = Non renseigné

    -   TXA-12.3 < = ClinicalDocument/id@root

    -   TXA-12.4 < = ISO

-   si ClinicalDocument/id@extension n'est pas renseigné :

    -   TXA-12.1 < = ClinicalDocument/id@root

    -   TXA-12.2 < = Non renseigné

    -   TXA-12.3 < = Non renseigné

    -   TXA-12.4 < = Non renseigné

##### Les données concernant la demande de traitement sur le document
###### Le groupe de segments OBXNTE portant le document CDA

Le message HL7 MDM contient un premier groupe OBXNTE composé :

-   d'un segment OBX contenant un document encodé en Base64 dont le type
    MIME est précisé en OBX-5.2, il peut s'agir d'un document CDA-R2
    Niv1 ou d'un CDA-R2 Niv3,

-   d'un segment PRT requis, pré-adopté de HL7v2.9, véhiculant les
    informations sur l'expéditeur du courriel MSSanté,

-   d'un segment PRT requis si connu et répétable, pré-adopté de HL7v2.9, véhiculant
    les informations sur  le(s) destinataire(s) du courriel MSSanté,

-   d'un segment PRT optionnel et répétable, pré-adopté de HL7v2.9, l’(es) adresse(s) mail sur la(les)quelle(s) le(s) destinataire(s) peut ou peuvent répondre.

Les champs des segments PRT doivent être renseignés conformément aux
spécifications [« Contraintes sur les types de données HL7 v2.5
applicables aux profils d'intégration du cadre technique IT
Infrastructure dans le périmètre d'IHE France » release 1.8](https://www.interopsante.org/publications).

Les tableaux suivants listent l'ensemble des **segments et des champs à
renseigner obligatoirement**, dans l'ordre indiqué, à l'exception du
dernier segment PRT permettant de préciser l'adresse mail de réponse
(qui est optionnel). Seuls les segments et les champs indiqués dans les
tableaux suivants sont à renseigner dans le message MDM :

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th colspan="3">
        <p>Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]</p>
      </th>
    </tr>
    <tr>
      <th>
        <p>Elément requis :</p>
      </th>
      <th>
        <p>Description :</p>
      </th>
      <th>
        <p>Valeur :</p>
      </th>
    </tr>
    <tr>
      <td>
        <p><strong>Segment OBX</strong></p>
      </td>
      <td>
        <p><strong>Observation/Result</strong></p>
      </td>
      <td>
        <p>Contient un document au format CDA-R2 </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-1</p>
      </td>
      <td>
        <p>Set Id - Obx</p>
      </td>
      <td>
        <p>Numéro de séquence du segment</p>
        <p><span class="hl7-color">1</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-2 </p>
      </td>
      <td>
        <p>Value Type</p>
      </td>
      <td>
        <p><span class="hl7-color">ED</span> (Encapsuled Data)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-3 = OBR-4</p>
      </td>
      <td>
        <p>Observation Identifier</p>
      </td>
      <td>
        <p><strong> </strong></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.1 : </p>
      </td>
      <td>
        <p>Code du Document</p>
      </td>
      <td rowspan="2">
        <p>Utiliser le <a href="https://ansforge.github.io/IG-terminologie-de-sante/ig/main/ValueSet-JDV-J07-XdsTypeCode-CISIS.html">JDV_J07-XdsTypeCode-CISIS</a> de la Nomenclature des Objets de Santé (NOS)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.2 : </p>
      </td>
      <td>
        <p>Libellé du Document</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt;OBX-3.3</p>
      </td>
      <td>
        <p>Système de codage dont est issu le code</p>
      </td>
      <td>
        <p><span class="hl7-color">LN</span> ou <span class="hl7-color">TRE_A05</span><a href="https://ansforge.github.io/IG-terminologie-de-sante/ig/main/CodeSystem-TRE-A05-TypeDocComplementaire.html"> (lien vers la TRE)</a> en fonction de l'appartenance du code à l'un de ces systèmes de codage.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-5 </p>
      </td>
      <td>
        <p>Observation Value</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.1</p>
      </td>
      <td>
        <p>Source Application</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.2</p>
      </td>
      <td>
        <p>Type</p>
      </td>
      <td>
        <p><span class="hl7-color">text</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.3</p>
      </td>
      <td>
        <p>Data Subtype</p>
      </td>
      <td>
        <p>Le champ prend la valeur <span class="hl7-color">XML</span>.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.4</p>
      </td>
      <td>
        <p>Encoding</p>
      </td>
      <td>
        <p><span class="hl7-color">Base64</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.5</p>
      </td>
      <td>
        <p>Data</p>
      </td>
      <td>
        <p>Intégrer le document CDA</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-11</p>
      </td>
      <td>
        <p>Observation Result Status</p>
      </td>
      <td>
        <p>Statut du document pris dans la table HL7 0085 (Observation Result Status Codes Interpretation)</p>
        <p>·       <span class="hl7-color">F</span> : Document validé</p>
        <p>·       <span class="hl7-color">D</span> : Document à supprimer</p>
        <p>·       <span class="hl7-color">C</span> : Remplacement du Document</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><strong>Segment PRT (Requis)</strong></p>
      </td>
      <td>
        <p><strong>Participation Information  Expéditeur</strong></p>
      </td>
      <td>
        <p>Ce segment contient les informations de l'expéditeur à l'origine de la demande de traitement sur le document.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-2 </p>
      </td>
      <td>
        <p>Action Code</p>
      </td>
      <td>
        <p><span class="hl7-color">UC</span> (Unchanged)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-4 </p>
      </td>
      <td>
        <p>Participation</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-4.1</p>
      </td>
      <td>
        <p>Code </p>
      </td>
      <td>
        <p><span class="hl7-color">SB</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-4.2</p>
      </td>
      <td>
        <p>Libellé du code</p>
      </td>
      <td>
        <p><span class="hl7-color">Send by</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-4.3</p>
      </td>
      <td>
        <p>Name Of Coding System</p>
      </td>
      <td>
        <p><span class="hl7-color">participation</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-5 (Requis si connu)</p>
      </td>
      <td>
        <p>Participation Person</p>
      </td>
      <td>
        <p>Ce champ est requis si connu si l'expéditeur est un professionnel de santé (Note 1).</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-5.1 (Requis si connu)</p>
      </td>
      <td>
        <p>ID number</p>
      </td>
      <td>
        <p>Identifiant du professionnel de santé expéditeur</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-5.2 (Requis si connu)</p>
      </td>
      <td>
        <p>Family Name</p>
      </td>
      <td>
        <p>Nom d'exercice de l'expéditeur</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-5.3 (Requis si connu)</p>
      </td>
      <td>
        <p>Given Name</p>
      </td>
      <td>
        <p>Prénom d'exercice de l'expéditeur</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-5.9 (Requis si connu)</p>
      </td>
      <td>
        <p>Assigning Authority</p>
      </td>
      <td>
        <p>Autorité d'affectation de l'identifiant de l'expéditeur </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-5.13 (Conditionnel)</p>
      </td>
      <td>
        <p>Identifier Type Code</p>
      </td>
      <td>
        <p>Le type d'identifiant (<a href="http://www.interopsante.org/offres/doc_inline_src/412/IHE_France_Constraints_on_HL7_data_types_for_ITI_v.1.7.3.pdf">Table 0203 - Interop'Santé</a>) est requis lorsque le PRT-5.1 est renseigné</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-8 (Requis si connu)</p>
      </td>
      <td>
        <p>Participation Organization</p>
      </td>
      <td>
        <p>Ce champ est requis si connu si l'expéditeur est une organisation (Note 1).</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-8.1 (Requis si connu)</p>
      </td>
      <td>
        <p>OrganizationName</p>
      </td>
      <td>
        <p>Nom de l'organisation</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-8.6 (Requis si connu)</p>
      </td>
      <td>
        <p>Assigning Authority</p>
      </td>
      <td>
        <p>Autorité d'affectation de l'identifiant de l'organisation expéditrice du document</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-8.7 (Requis si connu)</p>
      </td>
      <td>
        <p>Identifier Type Code</p>
      </td>
      <td>
        <p>Type d'identifiant (<a href="http://www.interopsante.org/offres/doc_inline_src/412/IHE_France_Constraints_on_HL7_data_types_for_ITI_v.1.7.3.pdf">Table 0203 - Interop'Santé</a>)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-8.10 (Requis si connu)</p>
      </td>
      <td>
        <p>Organization number</p>
      </td>
      <td>
        <p>Identifiant de l'organisation expéditrice du document</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-10 (Conditionnel)</p>
      </td>
      <td>
        <p>Participation Device</p>
      </td>
      <td>
        <p>Ce champ est requis si l'expéditeur est une application.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-10.1</p>
      </td>
      <td>
        <p>Entity Identifier</p>
      </td>
      <td>
        <p>Identifiant de l'application</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-15 (Requis)</p>
      </td>
      <td>
        <p>Participant Telecommunication Address</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-15.3</p>
      </td>
      <td>
        <p>Telecommunication Equipment Type</p>
      </td>
      <td>
        <p><span class="hl7-color">X.400</span> (X.400 email address)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-15.4</p>
      </td>
      <td>
        <p>Communication Address</p>
      </td>
      <td>
        <p>Intégrer l'adresse mail de l'expéditeur</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><strong>Segment PRT (Requis si connu)</strong></p>
      </td>
      <td>
        <p><strong>Participation Information  Destinataire</strong></p>
      </td>
      <td>
        <p>Contient les informations du destinataire initial du courriel MSSanté. Cf (Note 1), (Note 2).</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-2 </p>
      </td>
      <td>
        <p>Action Code</p>
      </td>
      <td>
        <p><span class="hl7-color">UC</span> (Unchanged)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-4 </p>
      </td>
      <td>
        <p>Participation</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-4.1</p>
      </td>
      <td>
        <p>Code </p>
      </td>
      <td>
        <p><span class="hl7-color">RCT</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-4.2</p>
      </td>
      <td>
        <p>Libellé du code</p>
      </td>
      <td>
        <p><span class="hl7-color">Result Copies To</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-4.3</p>
      </td>
      <td>
        <p>Name Of Coding System</p>
      </td>
      <td>
        <p><span class="hl7-color">participation</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-5 (Requis si connu)</p>
      </td>
      <td>
        <p>Participation Person</p>
      </td>
      <td>
        <p>Ce champ est requis si connu si le destinataire initial du courriel est un PS</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-5.1 (Requis si connu)</p>
      </td>
      <td>
        <p>ID number</p>
      </td>
      <td>
        <p>Identifiant du destinataire</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-5.2 (Requis si connu)</p>
      </td>
      <td>
        <p>Family Name</p>
      </td>
      <td>
        <p>Nom d'exercice du destinataire</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-5.3 (Requis si connu)</p>
      </td>
      <td>
        <p>Given Name</p>
      </td>
      <td>
        <p>Prénom d'exercice du destinataire</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-5.9 (Requis si connu)</p>
      </td>
      <td>
        <p>Assigning Authority</p>
      </td>
      <td>
        <p>Autorité d'affectation de l'identifiant du destinataire</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-5.13 (Conditionnel)</p>
      </td>
      <td>
        <p>Identifier Type Code</p>
      </td>
      <td>
        <p>Le type d'identifiant (<a href="http://www.interopsante.org/offres/doc_inline_src/412/IHE_France_Constraints_on_HL7_data_types_for_ITI_v.1.7.3.pdf">Table 0203 - Interop'Santé</a>) est requis lorsque le PRT-5.1 est renseigné</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-8 (Requis si connu)</p>
      </td>
      <td>
        <p>Participation Organization</p>
      </td>
      <td>
        <p>Ce champ permet de faciliter le traitement du document dans la bonne organisation au niveau du système CONSOMMATEUR (service, UF, pôle…). Cf (Note 3).</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-8.1 (Requis si connu)</p>
      </td>
      <td>
        <p>OrganizationName</p>
      </td>
      <td>
        <p>Nom du destinataire</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-8.6 (Requis si connu)</p>
      </td>
      <td>
        <p>Assigning Authority</p>
      </td>
      <td>
        <p>Autorité d'affectation de l'identifiant du destinataire</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-8.7 (Requis si connu)</p>
      </td>
      <td>
        <p>Identifier Type Code</p>
      </td>
      <td>
        <p>Type d'identifiant (<a href="http://www.interopsante.org/offres/doc_inline_src/412/IHE_France_Constraints_on_HL7_data_types_for_ITI_v.1.7.3.pdf">Table 0203 - Interop'Santé</a>)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-8.10 (Requis si connu)</p>
      </td>
      <td>
        <p>Organization number</p>
      </td>
      <td>
        <p>Identifiant du destinataire</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-15 (Requis)</p>
      </td>
      <td>
        <p>Participant Telecommunication Address</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-15.3</p>
      </td>
      <td>
        <p>Telecommunication Equipment Type</p>
      </td>
      <td>
        <p><span class="hl7-color">X.400</span> (X.400 email address)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-15.4</p>
      </td>
      <td>
        <p>Communication Address</p>
      </td>
      <td>
        <p>Intégrer l'adresse MSSanté du destinataire</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><strong>Segment PRT (segment optionnel)</strong></p>
      </td>
      <td>
        <p><strong>Participation Information adresse de réponse</strong></p>
      </td>
      <td>
        <p>Ce segment optionnel permet d'indiquer l'adresse mail sur laquelle le destinataire peut répondre.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-2 </p>
      </td>
      <td>
        <p>Action Code</p>
      </td>
      <td>
        <p><span class="hl7-color">UC</span> (Unchanged)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-4 </p>
      </td>
      <td>
        <p>Participation</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-4.1</p>
      </td>
      <td>
        <p>Code </p>
      </td>
      <td>
        <p><span class="hl7-color">REPLY</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-4.2</p>
      </td>
      <td>
        <p>Libellé du code</p>
      </td>
      <td>
        <p><span class="hl7-color">Reply To</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-4.3</p>
      </td>
      <td>
        <p>Name Of Coding System</p>
      </td>
      <td>
        <p><span class="hl7-color">participation</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>PRT-15 </p>
      </td>
      <td>
        <p>Participant Telecommunication Address</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-15.3</p>
      </td>
      <td>
        <p>Telecommunication Equipment Type</p>
      </td>
      <td>
        <p><span class="hl7-color">X.400</span> (X.400 email address)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; PRT-15.4</p>
      </td>
      <td>
        <p>Communication Address</p>
      </td>
      <td>
        <p>Intégrer l'adresse mail de réponse</p>
      </td>
    </tr>
  </tbody>
</table>

_**Note 1 :** le renseignement des informations concernant l’identification de l’expéditeur/destinataire est conditionné à la capacité du GESTIONNAIRE à interroger l’annuaire de l’établissement._

_**Note 2 :** en cas de transfert du courriel original au niveau de l’établissement destinataire, il n’est pas certain que l’acteur GESTIONNAIRE puisse récupérer l’information concernant le destinataire initial du courriel. Cette information peut être utilisée pour notifier au niveau du système CONSOMMATEUR, le PS ou le service clinique concerné par le courriel (organisation) du résultat du traitement réalisé sur le document par le système CONSOMMATEUR._

_**Note 3 :** dans la configuration où le GESTIONNAIRE est en capacité de maintenir une table de correspondance entre une BAL et une organisation correspondante (service clinique, UF, pôle…), le champ PRT-8 permet de préciser l’organisation de l’établissement concerné par la demande de traitement sur le document au niveau du CONSOMMATEUR. Dans le cas où le GESTIONNAIRE n’est pas en capacité de maintenir cette table de correspondance, le système CONSOMMATEUR peut prévoir un paramétrage pour associer une organisation de l’établissement (service clinique, UF, pôle…) à une BAL afin de réaliser le traitement sur le document dans la bonne organisation._

###### Le groupe de segments portant les informations du courriel MSSanté

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th colspan="3">
        <p>Composition du groupe OBXNTE : Usage = Required / Cardinalité = [1..1]</p>
      </th>
    </tr>
    <tr>
      <th>
        <p>Elément requis :</p>
      </th>
      <th>
        <p>Description :</p>
      </th>
      <th>
        <p>Valeur :</p>
      </th>
    </tr>
    <tr>
      <td>
        <p><strong>Segment OBX</strong></p>
      </td>
      <td>
        <p><strong>Observation/Result</strong></p>
      </td>
      <td>
        <p>Contient les informations du courriel MSSanté dont a été extrait le document</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-1</p>
      </td>
      <td>
        <p>Set Id - Obx</p>
      </td>
      <td>
        <p>Numéro de séquence du segment</p>
        <p><span class="hl7-color">2</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-2</p>
      </td>
      <td>
        <p>Value Type</p>
      </td>
      <td>
        <p><span class="hl7-color">ED</span> (Encapsulated Data)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-3 </p>
      </td>
      <td>
        <p>Observation Identifier</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.1 : </p>
      </td>
      <td>
        <p>Identifier</p>
      </td>
      <td>
        <p>Identifiant unique du courriel correspondant à l'élément Message-ID de l'entête du courriel MSSanté</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.2 : </p>
      </td>
      <td>
        <p>Text</p>
      </td>
      <td>
        <p>Objet du courriel</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-4 </p>
      </td>
      <td>
        <p>Observation Sub-id</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-5 </p>
      </td>
      <td>
        <p>Observation Value</p>
      </td>
      <td>
        <p>Contenu du courriel codé en base 64</p>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-11</p>
      </td>
      <td>
        <p>Observation Result Status</p>
      </td>
      <td>
        <p>Valeur fixée à « <span class="hl7-color">F</span> »</p>
      </td>
    </tr>
  </tbody>
</table>

###### Groupes OBXNTE portant les métadonnées MSSanté

Cette section présente uniquement les métadonnées de restriction indispensables aux échanges avec la MSSanté. Ces groupes sont conformes à ceux définis dans le volet « Transmission de documents CDA en HL7v2 » version 2.1

Les métadonnées peuvent être valorisées avec Y ou N suivant qu’elles sont activées ou non au moment de la validation du document.

Ces métadonnées sont requises et doivent apparaître dans le message MDM dans l’ordre présenté ci-dessous.

Pour l’ensemble des OBX listés dans cette section, le champ OBX-3 prend ses valeurs dans la [table « MetaDMP/MSS »](meta-dmp-mss.html). Le champ OBX-11 étant requis par le standard HL7v2, la valeur de ce champ est arbitrairement fixée à « F ».

####### Document Masqué aux professionnels de Santé

Cet OBX permet au Consommateur de vérifier que le document n'est pas masqué aux professionnels de santé.
<table class="table-hl7v2">
  <tbody>
    <tr>
      <th colspan="3">
        <p>Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]</p>
      </th>
    </tr>
    <tr>
      <th>
        <p>Elément requis :</p>
      </th>
      <th>
        <p>Description :</p>
      </th>
      <th>
        <p>Valeur :</p>
      </th>
    </tr>
    <tr>
      <td>
        <p><strong>Segment OBX</strong></p>
      </td>
      <td>
        <p><strong>Observation/Result</strong></p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-1</p>
      </td>
      <td>
        <p>Set Id - Obx</p>
      </td>
      <td>
        <p>Numéro de séquence du segment</p>
        <p><span class="hl7-color">3</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-2</p>
      </td>
      <td>
        <p>Value Type</p>
      </td>
      <td>
        <p><span class="hl7-color">CWE</span> (Coded with Exceptions)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-3</p>
      </td>
      <td>
        <p>Observation Identifier</p>
      </td>
      <td>
        <p><strong> </strong></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.1 : </p>
      </td>
      <td>
        <p>Code :</p>
      </td>
      <td>
        <p><span class="hl7-color">MASQUE_PS</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.2 : </p>
      </td>
      <td>
        <p>Libellé :</p>
      </td>
      <td>
        <p><span class="hl7-color">Masqué aux professionnels de Santé</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.3 :</p>
      </td>
      <td>
        <p>Name of Coding system</p>
      </td>
      <td>
        <p><span class="hl7-color">MetaDMPMSS</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-5</p>
      </td>
      <td>
        <p>Observation Value</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.1</p>
      </td>
      <td>
        <p>Code :</p>
      </td>
      <td>
        <p>Table HL7 : 0136 :</p>
        <p>·       <span class="hl7-color">N</span> (No) à MASQUE_PS non Actif</p>
        <p>·       <span class="hl7-color">Y</span> (Yes) à MASQUE_PS Actif</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.3</p>
      </td>
      <td>
        <p>Name Of Coding System</p>
      </td>
      <td>
        <p><span class="hl7-color">expandedYes-NoIndicator</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-11</p>
      </td>
      <td>
        <p>Observation Result Status</p>
      </td>
      <td>
        <p>Valeur fixée à « <span class="hl7-color">F</span> » </p>
      </td>
    </tr>
  </tbody>
</table>

####### Document Non visible par le patient

Cet OBX permet d'informer le Consommateur que le document est masqué ou non au patient.

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th colspan="3">
        <p>Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]</p>
      </th>
    </tr>
    <tr>
      <th>
        <p>Elément requis :</p>
      </th>
      <th>
        <p>Description :</p>
      </th>
      <th>
        <p>Valeur :</p>
      </th>
    </tr>
    <tr>
      <td>
        <p><strong>Segment OBX</strong></p>
      </td>
      <td>
        <p><strong>Observation/Result</strong></p>
      </td>
      <td>
        <p><strong> </strong></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-1</p>
      </td>
      <td>
        <p>Set Id - Obx</p>
      </td>
      <td>
        <p>Numéro de séquence du segment</p>
        <p><span class="hl7-color">4</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-2</p>
      </td>
      <td>
        <p>Value Type</p>
      </td>
      <td>
        <p><span class="hl7-color">CWE</span> (Coded with Exceptions)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-3</p>
      </td>
      <td>
        <p>Observation Identifier</p>
      </td>
      <td>
        <p><strong> </strong></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.1 : </p>
      </td>
      <td>
        <p>Code :</p>
      </td>
      <td>
        <p><span class="hl7-color">INVISIBLE_PATIENT</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.2 : </p>
      </td>
      <td>
        <p>Libellé :</p>
      </td>
      <td>
        <p><span class="hl7-color">Document Non Visible par le patient</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.3 :</p>
      </td>
      <td>
        <p>Name of Coding system</p>
      </td>
      <td>
        <p><span class="hl7-color">MetaDMPMSS</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-5</p>
      </td>
      <td>
        <p>Observation Value</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.1</p>
      </td>
      <td>
        <p>Code :</p>
      </td>
      <td>
        <p>Table HL7 : 0136 :</p>
        <p>·       <span class="hl7-color">Y</span> (YES) à INVISIBLE_PATIENT actif</p>
        <p>·       <span class="hl7-color">N</span> (No) à INVISIBLE_PATIENT non actif</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.3</p>
      </td>
      <td>
        <p>Name Of Coding System</p>
      </td>
      <td>
        <p><span class="hl7-color">expandedYes-NoIndicator</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-11</p>
      </td>
      <td>
        <p>Observation Result Status</p>
      </td>
      <td>
        <p>Valeur fixée à « <span class="hl7-color">F</span> » </p>
      </td>
    </tr>
  </tbody>
</table>

####### Document Non visible par les représentants légaux du patient

Cet OBX permet d'informer le Consommateur que le document est masqué ou non aux représentants légaux du patient.

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th colspan="3">
        <p>Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]</p>
      </th>
    </tr>
    <tr>
      <th>
        <p>Elément requis :</p>
      </th>
      <th>
        <p>Description :</p>
      </th>
      <th>
        <p>Valeur :</p>
      </th>
    </tr>
    <tr>
      <td>
        <p><strong>Segment OBX</strong></p>
      </td>
      <td>
        <p><strong>Observation/Result</strong></p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-1</p>
      </td>
      <td>
        <p>Set Id - Obx</p>
      </td>
      <td>
        <p>Numéro de séquence du segment</p>
        <p><span class="hl7-color">5</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-2</p>
      </td>
      <td>
        <p>Value Type</p>
      </td>
      <td>
        <p><span class="hl7-color">CWE</span> (Coded with Exceptions)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-3</p>
      </td>
      <td>
        <p>Observation Identifier</p>
      </td>
      <td>
        <p><strong> </strong></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.1 : </p>
      </td>
      <td>
        <p>Code :</p>
      </td>
      <td>
        <p><span class="hl7-color">INVISIBLE_ REP_LEGAUX</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.2 : </p>
      </td>
      <td>
        <p>Libellé :</p>
      </td>
      <td>
        <p><span class="hl7-color">Non visible par les représentants Légaux du patient</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.3 :</p>
      </td>
      <td>
        <p>Name of Coding system</p>
      </td>
      <td>
        <p><span class="hl7-color">MetaDMPMSS</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-5</p>
      </td>
      <td>
        <p>Observation Value</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.1</p>
      </td>
      <td>
        <p>Code :</p>
      </td>
      <td>
        <p>Table HL7 : 0136 :</p>
        <p>·       <span class="hl7-color">Y</span> (YES) à INVISIBLE_ REP_LEGAUX actif</p>
        <p>·       <span class="hl7-color">N</span> (No) à INVISIBLE_ REP_LEGAUX non actif</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.3</p>
      </td>
      <td>
        <p>Name Of Coding System</p>
      </td>
      <td>
        <p><span class="hl7-color">expandedYes-NoIndicator</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-11</p>
      </td>
      <td>
        <p>Observation Result Status</p>
      </td>
      <td>
        <p>Valeur fixée à « <span class="hl7-color">F</span> » </p>
      </td>
    </tr>
  </tbody>
</table>

####### Modification Confidentiality Code

Cet OBX permet d'informer le Consommateur que la transaction porte une modification du CONFIDENTIALITY CODE indiquant une mise à jour de la métadonnée de mise en visibilité du document au patients et/ou aux représentants légaux.

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th colspan="3">
        <p>Composition du groupe OBSERVATION/OBXNTE : Usage = Required / Cardinalité = [1..1]</p>
      </th>
    </tr>
    <tr>
      <th>
        <p>Elément requis :</p>
      </th>
      <th>
        <p>Description :</p>
      </th>
      <th>
        <p>Valeur :</p>
      </th>
    </tr>
    <tr>
      <td>
        <p><strong>Segment OBX</strong></p>
      </td>
      <td>
        <p><strong>Observation/Result</strong></p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-1</p>
      </td>
      <td>
        <p>Set Id - Obx</p>
      </td>
      <td>
        <p>Numéro de séquence du segment</p>
        <p><span class="hl7-color">6</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-2</p>
      </td>
      <td>
        <p>Value Type</p>
      </td>
      <td>
        <p><span class="hl7-color">CWE</span> (Coded with Exceptions)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-3</p>
      </td>
      <td>
        <p>Observation Identifier</p>
      </td>
      <td>
        <p><strong> </strong></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.1 : </p>
      </td>
      <td>
        <p>Code :</p>
      </td>
      <td>
        <p><span class="hl7-color">MODIF_CONF_CODE</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.2 : </p>
      </td>
      <td>
        <p>Libellé :</p>
      </td>
      <td>
        <p><span class="hl7-color">Modification Confidentiality Code</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-3.3 :</p>
      </td>
      <td>
        <p>Name of Coding system</p>
      </td>
      <td>
        <p><span class="hl7-color">MetaDMPMSS</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-5</p>
      </td>
      <td>
        <p>Observation Value</p>
      </td>
      <td>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.1</p>
      </td>
      <td>
        <p>Code :</p>
      </td>
      <td>
        <p>Table HL7 : 0136 :</p>
        <p>-        <span class="hl7-color">Y</span> (Yes) à MODIF_CONF_CODE actif</p>
        <p>-        <span class="hl7-color">N</span> (No) à MODIF_CONF_CODE non Actif</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>&gt; OBX-5.3</p>
      </td>
      <td>
        <p>Name Of Coding System</p>
      </td>
      <td>
        <p><span class="hl7-color">expandedYes-NoIndicator</span></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>OBX-11</p>
      </td>
      <td>
        <p>Observation Result Status</p>
      </td>
      <td>
        <p>Valeur fixée à « <span class="hl7-color">F</span> » </p>
      </td>
    </tr>
  </tbody>
</table>

Un exemple est disponible [ici](exemples.html).

#### Le message d'acquittement HL7v2

##### Profil du message ACK

Le profil du message ACK est le suivant :

<table class="table-hl7v2">
  <tr>
    <th>
      <p>Segment</p>
    </th>
    <th>
      <p>Meaning</p>
    </th>
    <th>
      <p>Usage</p>
    </th>
    <th>
      <p>Card.</p>
    </th>
    <th>
      <p>HL7 §</p>
    </th>
  </tr>
  <tbody>
    <tr>
      <td>
        <p>MSH</p>
      </td>
      <td>
        <p>Message header</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p>2</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>[{SFT}]</p>
      </td>
      <td>
        <p>Software segment</p>
      </td>
      <td>
        <p>O</p>
      </td>
      <td>
        <p>[0..*]</p>
      </td>
      <td>
        <p>2</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>[UAC]</p>
      </td>
      <td>
        <p>User Authentication Credential</p>
      </td>
      <td>
        <p>O</p>
      </td>
      <td>
        <p>[0..1]</p>
      </td>
      <td>
        <p>2</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSA</p>
      </td>
      <td>
        <p>Message Acknowledgement</p>
      </td>
      <td>
        <p>R</p>
      </td>
      <td>
        <p>[1..1]</p>
      </td>
      <td>
        <p>2</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>[{ERR}]</p>
      </td>
      <td>
        <p>Error</p>
      </td>
      <td>
        <p>C</p>
      </td>
      <td>
        <p>[0..*]</p>
      </td>
      <td>
        <p>2</p>
      </td>
    </tr>
  </tbody>
</table>

##### Structure fonctionnelle du message

Après réception du message MDM, le LPS (DPI ou RIS dans le contexte SEGUR vague 2) va acquitter le message. Ci-dessous la structure du message ACK :
<div class="figure" style='text-align: center;'>
    <img src="image21.png" alt="Figure 15" title="Figure 15 : Description fonctionnelle du message ACK
" style="width:80%;">
    <figcaption><b>Figure 15 : Description fonctionnelle du message ACK</b></figcaption>
</div>    
<br>
Ces segments doivent être conformes au standard HL7v2.6.

##### Description des contraintes à appliquer sur le message ACK

###### Segment MSH

Le segment MSH reprend une partie des informations du message initial :

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th colspan="2">
        <p>Message initial</p>
      </th>
      <th colspan="2">
        <p>Message d'acquittement</p>
      </th>
    </tr>
    <tr>
      <th>
        <p>Champ</p>
      </th>
      <th>
        <p>Description</p>
      </th>
      <th>
        <p>Champ</p>
      </th>
      <th>
        <p>Description</p>
      </th>
    </tr>
    <tr>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.3">MSH.3</a> - Sending Application​</p>
      </td>
      <td>
        <p>Application source du message à acquitter</p>
      </td>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.5">MSH.5</a> - Receiving Application​</p>
      </td>
      <td>
        <p>Application destinatrice de l'acquittement</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.4">MSH.4</a> - Sending Facility​</p>
      </td>
      <td>
        <p>Facility source du message à acquitter</p>
      </td>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6">MSH.6</a> - Receiving Facility​</p>
      </td>
      <td>
        <p>Etablissement destinataire de l'acquittement</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.5">MSH.5</a> - Receiving Application​</p>
      </td>
      <td>
        <p>Application destinatrice du message à acquitter</p>
      </td>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.3">MSH.3</a> - Sending Application​</p>
      </td>
      <td>
        <p>Application source de l'acquittement</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6">MSH.6</a> - Receiving Facility​</p>
      </td>
      <td>
        <p>Facility destinatrice du message à acquitter</p>
      </td>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.4">MSH.4</a> - Sending Facility​</p>
      </td>
      <td>
        <p>Etablissement source de l'acquittement</p>
      </td>
    </tr>
    <tr>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.11">MSH.11</a> - Processing Id​</p>
      </td>
      <td>
        <p>Identifiant de traitement</p>
      </td>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.11">MSH.11</a> - Processing Id​</p>
      </td>
      <td>
        <p>Identifiant de traitement</p>
      </td>
    </tr>
  </tbody>
</table>

Le champ MSH.9 « Message type » prend la valeur : `ACK^T02^ACK` ou `ACK^T04^ACK` ou `ACK^T10^ACK` selon l’évènement du message initial.

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th>
        <p>Champ</p>
      </th>
      <th>
        <p>Contenu</p>
      </th>
      <th>
        <p>Type donnée</p>
      </th>
      <th>
        <p>Caractère optionnel/obligatoire</p>
        <p> </p>
        <p> </p>
      </th>
    </tr>
    <tr>
      <td>
        <p>MSH-1</p>
      </td>
      <td>
        <p><span class="hl7-color">|</span> séparateur de champ</p>
      </td>
      <td>
        <p>ST</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-2</p>
      </td>
      <td>
        <p><span class="hl7-color">^~\&</span> : séparateur de composant, répétition, caractère d'échappement, séparateur de sous-composants</p>
      </td>
      <td>
        <p>ST</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-3</p>
      </td>
      <td>
        <p>Application émettrice</p>
      </td>
      <td>
        <p>HD</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-4</p>
      </td>
      <td>
        <p>Organisation émettrice</p>
      </td>
      <td>
        <p>HD</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-5</p>
      </td>
      <td>
        <p>Application réceptrice</p>
      </td>
      <td>
        <p>HD</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-6</p>
      </td>
      <td>
        <p>Organisation réceptrice</p>
      </td>
      <td>
        <p>HD</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-7</p>
      </td>
      <td>
        <p>Date/time du message</p>
      </td>
      <td>
        <p>TS</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-9</p>
      </td>
      <td>
        <p>Type du message, selon l'évènement du message initial :</p>
        <p><span class="hl7-color">ACK^T02^ACK</span></p>
        <p><span class="hl7-color">ACK^T04^ACK</span></p> 
        <p><span class="hl7-color">ACK^T10^ACK</span></p>
        <p> </p>
      </td>
      <td>
        <p>MSG</p>
      </td>
      <td>
        <p>R</p>
        <p> </p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-10</p>
      </td>
      <td>
        <p>Identifiant du message</p>
      </td>
      <td>
        <p>ST</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-11</p>
      </td>
      <td>
        <p>Processing Id</p>
        <p><span class="hl7-color">P</span> : en production</p>
        <p><span class="hl7-color">T</span> : message de test</p>
        <p><span class="hl7-color">D</span> : environnement de debug</p>
      </td>
      <td>
        <p>PT</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-12</p>
      </td>
      <td>
        <p>Version du standard <span class="hl7-color">2.6</span> pour MDM</p>
      </td>
      <td>
        <p>VID</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-17</p>
      </td>
      <td>
        <p><span class="hl7-color">FRA</span></p>
      </td>
      <td>
        <p>ID</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>MSH-18</p>
      </td>
      <td>
        <p>Jeux de caractères, valeurs possibles :</p>
        <p><span class="hl7-color">UNICODE UTF-8</span> ou <span class="hl7-color">8859/15</span></p>
      </td>
      <td>
        <p>ID</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
  </tbody>
</table>

###### Segment MSA

Le segment MSA contient à minima les champs suivants : 

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th>
        <p>Champ requis</p>
      </th>
      <th>
        <p>Contenu</p>
      </th>
    </tr>
    <tr>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6">MSA.1</a> - Acknowledgment Code</p>
      </td>
      <td>
        <p>Code d'acquittement du message :</p>
        <p>·       AA (Original mode: Application Accept - Enhanced mode: Application acknowledgment: Accept) : le message a été compris et intégré par l'application destinatrice qui prend la responsabilité du message et libère ainsi l'application productrice de toute obligation de le renvoyer.</p>
        <p>·       AE (Original mode: Application Error - Enhanced mode: Application acknowledgment: Error) : le message contient des erreurs de syntaxe.   </p>
        <p>·       AR (Original mode: Application Reject - Enhanced mode: Application acknowledgment: Reject) : le message est rejeté pour une raison circonstancielle. Il peut être réémis plus tard. </p>
      </td>
    </tr>
    <tr>
      <td>
        <p><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6">MSA.2</a> - Message Control Id</p>
      </td>
      <td>
        <p>Rappel l'identifiant du message acquitté correspondant au champ MSH.10 du message initial.</p>
      </td>
    </tr>
  </tbody>
</table>

###### Segment ERR

Ce segment est utilisé au niveau des messages d'acquittement HL7 dans le cas où le champ MSA-1 prend la valeur AE (Application error).

Le tableau ci-dessous liste les champs à renseigner pour le segment ERR :

<table class="table-hl7v2">
  <tbody>
    <tr>
      <th>
        <p>Champ</p>
      </th>
      <th>
        <p>Contenu</p>
      </th>
      <th>
        <p>Type donnée</p>
      </th>
      <th>
        <p>Caractère optionnel/obligatoire</p>
      </th>
    </tr>
    <tr>
      <td>
        <p>ERR-2</p>
      </td>
      <td>
        <p>Localisation de l'erreur dans le cas d'une erreur de syntaxe du message initial.</p>
      </td>
      <td>
        <p>ERL</p>
      </td>
      <td>
        <p>O</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>ERR-3</p>
      </td>
      <td>
        <p>Code erreur HL7 dont les valeurs sont à prendre dans la table HL7 0357 (nom symbolique : messageErrorCondition)</p>
      </td>
      <td>
        <p>CWE</p>
      </td>
      <td>
        <p>R(Note 1) (Note 2)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>ERR-4</p>
      </td>
      <td>
        <p>Sévérité de l'erreur dont les valeurs sont à prendre dans la table HL7 0516 (nom symbolique : errorSeverity)</p>
      </td>
      <td>
        <p>ID</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>ERR-5</p>
      </td>
      <td>
        <p>Code erreur du traitement applicatif du message HL7 dont les valeurs sont à prendre dans la table user-defined 0533 (nom symbolique : applicationErrorCode)</p>
      </td>
      <td>
        <p>CWE</p>
      </td>
      <td>
        <p>C(Note 1) (Note 2)</p>
      </td>
    </tr>
  </tbody>
</table>

_**(Note 1) :** les valeurs possibles pour les champs ERR-3 et ERR-5 sont listées dans les tables messageErrorCondition et applicationErrorCondition précisées [ici](error-codes.html)._

_**Note (2) :** dans le cas où le rejet du message HL7 MDM est dû à un problème applicatif au niveau du CONSOMMATEUR, le champ ERR-3 sera renseigné avec la valeur « 207 » (Application error) et le champ ERR-5 sera renseigné avec une valeur comprise dans la table applicationErrorCode. Dans le cas où le message MDM est rejeté par le système CONSOMMATEUR pour une raison technique, le champ ERR-3 sera renseigné avec une valeur comprise dans la table messageErrorCondition et le champ ERR-5 ne sera pas renseigné._

###### Exemple

Entête MSH d'un message MDM émis par le GESTIONNAIRE vers le CONSOMMATEUR :

```
MSH|^~\&|PFI|CHU_X|DPI|CHU_X|202310030830||MDM^T02^MDM_T02|12345|P|2.6|||||FRA|8859/15|||1.1^ CISIS_CDA_HL7_LPS
```
Un acquittement positif retourné par le CONSOMMATEUR :

```
MSH|^~\&|DPI|CHU_X|PFI|CHU_X|202310030831||ACK^T02^ACK|12346|P|2.6|||AL|AL|FRA|8859/15
MSA|AA|12345
```

Un acquittement négatif retourné par le CONSOMMATEUR : version d'HL7 inconnue

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