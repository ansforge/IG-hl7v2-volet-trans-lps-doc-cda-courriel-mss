### Le message MDM en HL7 v2.6

#### Description du profil du message MDM
Le profil du message MDM est le suivant :
<table style="background-color: grey;">
<thead>
<tr>
<td width="104">
<p>Segment</p>
</td>
<td width="274">
<p>Meaning</p>
</td>
<td width="64">
<p>Usage</p>
</td>
<td width="82">
<p>Card.</p>
</td>
<td width="66">
<p>&sect; HL7</p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td width="104">
<p>MSH</p>
</td>
<td width="274">
<p>Message Header</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..1]</p>
</td>
<td width="66">
<p>2</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp;[{SFT}]</p>
</td>
<td width="274">
<p>Software Segment</p>
</td>
<td width="64">
<p>O</p>
</td>
<td width="82">
<p>[0..*]</p>
</td>
<td width="66">
<p>2</p>
</td>
</tr>
<tr>
<td width="104">
<p>[UAC]</p>
</td>
<td width="274">
<p>User Authentication Credentials</p>
</td>
<td width="64">
<p>O</p>
</td>
<td width="82">
<p>[0..1]</p>
</td>
<td width="66">
<p>2</p>
</td>
</tr>
<tr>
<td width="104">
<p>EVN</p>
</td>
<td width="274">
<p>Event type</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..1]</p>
</td>
<td width="66">
<p>2</p>
</td>
</tr>
<tr>
<td width="104">
<p>PID</p>
</td>
<td width="274">
<p>Patient Identification</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..1]</p>
</td>
<td width="66">
<p>3</p>
</td>
</tr>
<tr>
<td width="104">
<p>PV1</p>
</td>
<td width="274">
<p>Patient Visit</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..1]</p>
</td>
<td width="66">
<p>3</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp;</p>
</td>
<td width="274">
<p>--- COMMON_ORDER begin</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..1]</p>
</td>
<td width="66">
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp;ORC</p>
</td>
<td width="274">
<p>Common Order = demande de service sur le document</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..1]</p>
</td>
<td width="66">
<p>4</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp;[{</p>
</td>
<td width="274">
<p>--- TIMING begin</p>
</td>
<td width="64">
<p>O</p>
</td>
<td width="82">
<p>[0..*]</p>
</td>
<td width="66">
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp; TQ1</p>
</td>
<td width="274">
<p>Timing/Quantity</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..1]</p>
</td>
<td width="66">
<p>4</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp; [{TQ2}]</p>
</td>
<td width="274">
<p>Timing/Quantity RelationShip</p>
</td>
<td width="64">
<p>O</p>
</td>
<td width="82">
<p>[0..*]</p>
</td>
<td width="66">
<p>4</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp;}]</p>
</td>
<td width="274">
<p>--- TIMING end</p>
</td>
<td width="64">
<p>&nbsp;</p>
</td>
<td width="82">
<p>&nbsp;</p>
</td>
<td width="66">
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp;OBR</p>
</td>
<td width="274">
<p>Observation Request segment</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..1]</p>
</td>
<td width="66">
<p>4</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp;[{NTE}]</p>
</td>
<td width="274">
<p>Notes and comments</p>
</td>
<td width="64">
<p>O</p>
</td>
<td width="82">
<p>[0..*]</p>
</td>
<td width="66">
<p>2</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp;</p>
</td>
<td width="274">
<p>--- COMMON_ORDER end</p>
</td>
<td width="64">
<p>&nbsp;</p>
</td>
<td width="82">
<p>&nbsp;</p>
</td>
<td width="66">
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td width="104">
<p>TXA</p>
</td>
<td width="274">
<p>Transcription document header</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..1]</p>
</td>
<td width="66">
<p>9</p>
</td>
</tr>
<tr>
<td width="104">
<p>{</p>
</td>
<td width="274">
<p>OBXNTE (Document, informations sur le courriel, m&eacute;tadonn&eacute;es sur le document)</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..*]</p>
</td>
<td width="66">
<p>&nbsp;</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp;OBX</p>
</td>
<td width="274">
<p>Observation/Result</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..1]</p>
</td>
<td width="66">
<p>9</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp;[{PRT}]</p>
</td>
<td width="274">
<p>Participation : Exp&eacute;diteur, destinataire(s) MSS et adresse mail sur laquelle le destinataire peut r&eacute;pondre. Segment PRT pr&eacute;-adopt&eacute; de la version 2.9</p>
</td>
<td width="64">
<p>R</p>
</td>
<td width="82">
<p>[1..*]</p>
</td>
<td width="66">
<p>7 (v2.9)</p>
</td>
</tr>
<tr>
<td width="104">
<p>&nbsp;[{NTE}]</p>
</td>
<td width="274">
<p>Notes and comments</p>
</td>
<td width="64">
<p>O</p>
</td>
<td width="82">
<p>[0..*]</p>
</td>
<td width="66">
<p>2</p>
</td>
</tr>
<tr>
<td width="104">
<p>}</p>
</td>
<td width="274">
<p>---OBXNTE end</p>
</td>
<td width="64">
<p>&nbsp;</p>
</td>
<td width="82">
<p>&nbsp;</p>
</td>
<td width="66">
<p>&nbsp;</p>
</td>
</tr>
</tbody>
</table>

Le message HL7 MDM ne peut transmettre qu’un seul document médical.

Les contraintes apportées par ce volet sur les données du message MDM sont décrites à la [section dédiée](profils-messages.html#contraintes-appliquées-aux-messages-mdm-dans-le-contexte-de-ce-volet).

#### Description fonctionnelle du message MDM

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
    (contraintes décrites au [paragraphe dédié](profils-messages.html#le-groupe-de-segments-obxnte-portant-le-document-cda)).

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

### Contraintes appliquées aux messages MDM dans le contexte de ce volet
Dans la suite de cette section, les valeurs indiquées en bleu dans les tableaux indiquent les valeurs fixes à insérer dans le champ du message.

#### Eléments de contrôle du message MDM

##### Le segment MSH – Header du message

<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" style="border-collapse:collapse;mso-table-layout-alt:fixed;border:none;
 mso-border-alt:solid windowtext .5pt;mso-yfti-tbllook:1184;mso-padding-alt:
 0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:46.5pt">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;
  height:46.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Champ<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:46.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Contenu<o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:46.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Type donnée<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:46.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Caractère
  optionnel/obligatoire<o:p></o:p></span></span></p>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black"><o:p>&nbsp;</o:p></span></span></p>
  <span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-1<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:#4472C4;mso-themecolor:accent5">|</span><span style="color:black">
  séparateur de champ<o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">ST<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-2<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:#4472C4;mso-themecolor:accent5">^~\&amp;</span><span style="color:black">&nbsp;: séparateur de composant, répétition, caractère
  d’échappement, séparateur de sous-composants<o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">ST<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-3<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Application émettrice<o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">HD<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:4">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-4<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Organisation émettrice<o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">HD<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:5">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-5<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Application réceptrice<o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">HD<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:6">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-6<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Organisation réceptrice<o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">HD<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:7">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-7<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Date/time du message<o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">TS<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:8">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-9<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Type du message<br>
  </span><span style="color:#4472C4;mso-themecolor:accent5">MDM^T02^MDM_T02<br>
  MDM^T10^MDM_T02<br>
  MDM^T04^MDM_T02</span><span style="color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSG<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  <span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:9">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-10<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Identifiant du message<o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">ST<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:10">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-11<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647"><span class="SpellE"><span style="color:black">Processing</span></span><span style="color:black"> Id<br>
  </span><span style="color:#4472C4;mso-themecolor:accent5">P&nbsp;</span>: en
  production<span style="color:#4472C4;mso-themecolor:accent5"><br>
  T&nbsp;</span>: message de test<span style="color:#4472C4;mso-themecolor:
  accent5"><br>
  D&nbsp;</span>: environnement de <span class="SpellE">debug</span><span style="color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">PT<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:11">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-12<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647"><span style="color:black">Version du standard<br>
  </span><span style="color:#4472C4;mso-themecolor:accent5">2.6 </span><span style="color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">VID<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:12">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-17<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:#4472C4;mso-themecolor:accent5">FRA</span><span style="color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">ID<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:13">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-18<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Jeux de caractères, valeurs possibles&nbsp;:<o:p></o:p></span></span></p>
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647"><span style="color:#4472C4;mso-themecolor:accent5">UNICODE
  UTF-8 </span>ou<span style="color:#4472C4;mso-themecolor:accent5"> 8859/15 </span><span style="color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">ID<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:14;mso-yfti-lastrow:yes">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-21<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.55pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Identifiant du profil de message<o:p></o:p></span></span></p>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">MSH-21.1&nbsp;: <span class="SpellE">Entity</span>
  Identifier (</span><span style="color:#4472C4;mso-themecolor:accent5">1.1</span><span style="color:black">)<o:p></o:p></span></span></p>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="color:black;mso-ansi-language:EN-US">MSH-21.<span class="GramE">2&nbsp;:</span>
  Namespace Id<o:p></o:p></span></span></p>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#4472C4;mso-themecolor:accent5;mso-ansi-language:EN-US;mso-bidi-font-weight:
  bold">CISIS_CDA_HL7_LPS</span></span><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="color:black;mso-ansi-language:EN-US"><o:p></o:p></span></span></p>
  </td>
  
  <td width="104" valign="top" style="width:77.95pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">EI<o:p></o:p></span></span></p>
  </td>
  
  <td width="151" valign="top" style="width:4.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
</tbody></table>

#####  Exemples

Entête MSH d’un message MDM émis par le GESTIONNAIRE :

`MSH|^~\&|PFI|CHU_X|DPI|CHU_X|202310030830||MDM^T02^MDM^T02^MDM_T02|12345|P|2.6|||||FRA|8859/15|||1.1^ CISIS_CDA_HL7_LPS`

#### Les données concernant le patient et la venue du patient

Le message HL7 MDM est centré sur un seul patient. Les informations concernant le patient sont décrites par le segment requis PID. Le segment PV1, requis dans le standard, représente la venue courante du patient.

Ces deux segments doivent être renseignés conformément à la spécification « [PAM – National extension France » version 2.11](https://old.interopsante.org/offres/doc_inline_src/412/Publication-IHE_FRANCE_PAM_National_Extension_v2.11.pdf) publiée en 2024. Si l’INS est véhiculé, le segment PID doit suivre les contraintes décrites dans l’[annexe CI-SIS « Prise en charge de l’identifiant National de Santé (INS) dans les standards d’interopérabilité et les volets du CI-SIS »](https://esante.gouv.fr/sites/default/files/media_entity/documents/ans_cisis-tec_annexe-ins_1.5.pdf).
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="699" style="border-collapse:collapse;mso-table-layout-alt:fixed;border:none;
 mso-border-alt:solid windowtext .5pt;mso-yfti-tbllook:1184;mso-padding-alt:
 0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:23.5pt">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;
  height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Champ<o:p></o:p></span></span></p>
  </td>
  
  <td width="283" valign="top" style="width:212.6pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Contenu<o:p></o:p></span></span></p>
  </td>
  
  <td width="76" valign="top" style="width:2.0cm;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Type donnée<o:p></o:p></span></span></p>
  </td>
  
  <td width="246" valign="top" style="width:184.3pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Caractère
  optionnel/obligatoire <o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">PID-3<o:p></o:p></span></span></p>
  </td>
  
  <td width="283" valign="top" style="width:212.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="mso-bidi-font-family:Arial;color:black">Identifiants du patient<o:p></o:p></span></span></p>
  </td>
  
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">CX<o:p></o:p></span></span></p>
  </td>
  
  <td width="246" valign="top" style="width:184.3pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:2;mso-yfti-lastrow:yes">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">PID-5<o:p></o:p></span></span></p>
  </td>
  
  <td width="283" valign="top" style="width:212.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647">Nom du patient</span></p>
  </td>
  
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">XPN<o:p></o:p></span></span></p>
  </td>
  
  <td width="246" valign="top" style="width:184.3pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
</tbody></table>
Le PID-3 doit être identique aux identifiants de patient portés par le document CDA (recordTarget/patientRole/id).

Pour le segment PV1, ce volet ajoute les contraintes suivantes :
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="699" style="border-collapse:collapse;mso-table-layout-alt:fixed;border:none;
 mso-border-alt:solid windowtext .5pt;mso-yfti-tbllook:1184;mso-padding-alt:
 0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:23.5pt">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;
  height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Champ<o:p></o:p></span></span></p>
  </td>
  
  <td width="302" valign="top" style="width:8.0cm;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Contenu<o:p></o:p></span></span></p>
  </td>
  
  <td width="113" valign="top" style="width:3.0cm;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Type donnée<o:p></o:p></span></span></p>
  </td>
  
  <td width="189" valign="top" style="width:5.0cm;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Caractère
  optionnel/obligatoire<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:1;mso-yfti-lastrow:yes">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">PV1-2<o:p></o:p></span></span></p>
  </td>
  
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647"><span style="mso-bidi-font-family:Arial;color:black">Classe du
  patient&nbsp;: </span></span><span style="mso-bookmark:_Toc23346647"><span style="mso-bidi-font-family:Arial;color:#4472C4;mso-themecolor:accent5">N </span></span><span style="mso-bookmark:_Toc23346647"><span style="mso-bidi-font-family:Arial">(Not
  applicable)<span style="color:black"><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="113" valign="top" style="width:3.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">IS<o:p></o:p></span></span></p>
  </td>
  
  <td width="189" valign="top" style="width:5.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R <o:p></o:p></span></span></p>
  </td>
  
 </tr>
</tbody></table>

#### Le segment ORC
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="652" style="width:488.8pt;border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes">
  <td width="652" colspan="3" valign="top" style="width:488.8pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#E5E5E5;mso-shading:windowtext;
  mso-pattern:gray-10 auto;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Composition du segment
  ORC&nbsp;: Usage&nbsp;= <span class="SpellE">Required</span> /
  Cardinalité&nbsp;= [<span class="GramE">1..</span>1]<o:p></o:p></span></b></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="201" valign="top" style="width:150.8pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  background:#E5E5E5;mso-shading:windowtext;mso-pattern:gray-10 auto;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Elément requis&nbsp;:<o:p></o:p></span></b></span></p>
  </td>
  
  <td width="177" valign="top" style="width:132.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#E5E5E5;mso-shading:windowtext;
  mso-pattern:gray-10 auto;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Description&nbsp;: <o:p></o:p></span></b></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#E5E5E5;mso-shading:windowtext;
  mso-pattern:gray-10 auto;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Valeur&nbsp;: <o:p></o:p></span></b></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="201" valign="top" style="width:150.8pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Segment ORC<o:p></o:p></span></b></span></p>
  </td>
  
  <td width="177" valign="top" style="width:132.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Common <span class="SpellE">Order</span><o:p></o:p></span></b></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold"><span style="mso-spacerun:yes">&nbsp;</span><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:3;mso-yfti-lastrow:yes">
  <td width="201" valign="top" style="width:150.8pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">ORC-1<o:p></o:p></span></span></p>
  </td>
  
  <td width="177" valign="top" style="width:132.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Order</span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold">
  control<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">NW </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold">(New <span class="SpellE">order</span>/service dans le cas d’une demande d’intégration de
  document(s)<o:p></o:p></span></span></p>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">RO </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold">(Replace
  <span class="SpellE">order</span>) dans le cas d’une demande de remplacement<o:p></o:p></span></span></p>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">CA </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold">(<span class="SpellE">Canceled</span>) dans le cas d’une demande de suppression<o:p></o:p></span></span></p>
  </td>
  
 </tr>
</tbody></table>

#### Le segment OBR

<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="652" style="width:488.8pt;border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes">
  <td width="652" colspan="3" valign="top" style="width:488.8pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#E5E5E5;mso-shading:windowtext;
  mso-pattern:gray-10 auto;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Composition du segment
  OBR&nbsp;: Usage&nbsp;= <span class="SpellE">Required</span> /
  Cardinalité&nbsp;= [<span class="GramE">1..</span>1]<o:p></o:p></span></b></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="201" valign="top" style="width:150.8pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  background:#E5E5E5;mso-shading:windowtext;mso-pattern:gray-10 auto;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Elément requis&nbsp;:<o:p></o:p></span></b></span></p>
  </td>
  
  <td width="177" valign="top" style="width:132.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#E5E5E5;mso-shading:windowtext;
  mso-pattern:gray-10 auto;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Description&nbsp;: <o:p></o:p></span></b></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#E5E5E5;mso-shading:windowtext;
  mso-pattern:gray-10 auto;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Valeur&nbsp;: <o:p></o:p></span></b></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="201" valign="top" style="width:150.8pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Segment OBR<o:p></o:p></span></b></span></p>
  </td>
  
  <td width="177" valign="top" style="width:132.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Observation <span class="SpellE">Request</span><o:p></o:p></span></b></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold"><span style="mso-spacerun:yes">&nbsp;</span><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="201" valign="top" style="width:150.8pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">OBR-4<o:p></o:p></span></span></p>
  </td>
  
  <td width="177" valign="top" style="width:132.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Universal Service Identifier<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:4">
  <td width="201" valign="top" style="width:150.8pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt;OBR-4.1<o:p></o:p></span></span></p>
  </td>
  
  <td width="177" valign="top" style="width:132.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Code du document<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" rowspan="2" valign="top" style="width:205.5pt;border-top:none;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Utiliser le </span></span><a href="https://mos.esante.gouv.fr/NOS/JDV_J07-XdsTypeCode-CISIS/JDV_J07-XdsTypeCode-CISIS.pdf"><span style="mso-bookmark:_Toc23346647">JDV_J07-XdsTypeCode-CISIS</span></a><span style="mso-bookmark:_Toc23346647"> d</span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">e la Nomenclature des Objets de Santé (NOS). <o:p></o:p></span></span></p>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">A noter qu’en cas d’envoi au DMP, le Gestionnaire doit contrôler
  que le type de document appartient au jeu de valeur défini par le DMP (</span></span><a href="https://mos.esante.gouv.fr/NOS/JDV_J66-TypeCode-DMP/"><span style="mso-bookmark:_Toc23346647">JDV_J66-TypeCode-DMP</span></a><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">).<span style="mso-bidi-font-weight:
  bold"><o:p></o:p></span></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:5">
  <td width="201" valign="top" style="width:150.8pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt;OBR-4.2<o:p></o:p></span></span></p>
  </td>
  
  <td width="177" valign="top" style="width:132.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Libellé du document<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:6;mso-yfti-lastrow:yes">
  <td width="201" valign="top" style="width:150.8pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt;OBR-4.3<o:p></o:p></span></span></p>
  </td>
  
  <td width="177" valign="top" style="width:132.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Système de codage dont est issu le
  code<o:p></o:p></span></span></p>
  </td>
  
  <td width="274" valign="top" style="width:205.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">LN </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;mso-bidi-font-weight:bold">ou <span style="color:#0070C0">TRE_A05 </span><span style="color:black">en fonction de
  l’appartenance du code à l’un des trois systèmes de codage<o:p></o:p></span></span></span></p>
  </td>
  
 </tr>
</tbody></table>

#### Les données d’entête du document – Segment TXA

Le message MDM requiert l’utilisation du segment TXA qui porte les métadonnées associées au document contenu dans le message. Les contraintes apportées par ce volet sur le segment TXA sont les suivantes :
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="699" style="border-collapse:collapse;mso-table-layout-alt:fixed;border:none;
 mso-border-alt:solid windowtext .5pt;mso-yfti-tbllook:1184;mso-padding-alt:
 0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:23.5pt">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;
  height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Champ<o:p></o:p></span></span></p>
  </td>
  
  <td width="350" valign="top" style="width:262.25pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Contenu<o:p></o:p></span></span></p>
  </td>
  
  <td width="76" valign="top" style="width:2.0cm;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Type donnée<o:p></o:p></span></span></p>
  </td>
  
  <td width="180" valign="top" style="width:134.65pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="mso-bookmark:_Toc23346647"><span style="color:black">Caractère
  optionnel/obligatoire<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">TXA-1<o:p></o:p></span></span></p>
  </td>
  
  <td width="350" valign="top" style="width:262.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="mso-bidi-font-family:Arial;color:black">Set-ID TXA. Valeur = </span></span><span style="mso-bookmark:_Toc23346647"><span style="mso-bidi-font-family:Arial;
  color:#2E74B5;mso-themecolor:accent1;mso-themeshade:191">1</span></span><span style="mso-bookmark:_Toc23346647"><span style="mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">SI<o:p></o:p></span></span></p>
  </td>
  
  <td width="180" valign="top" style="width:134.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">TXA-2<o:p></o:p></span></span></p>
  </td>
  
  <td width="350" valign="top" style="width:262.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647">Type de document
  dont les valeurs sont à prendre dans </span><span style="mso-bookmark:_Toc23346647"><span style="mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="GramE"><span style="mso-bidi-font-family:Arial;color:black">le</span></span></span><span style="mso-bookmark:_Toc23346647"><span style="mso-bidi-font-family:Arial;
  color:black"> </span></span><a href="https://mos.esante.gouv.fr/NOS/JDV_J07-XdsTypeCode-CISIS/JDV_J07-XdsTypeCode-CISIS.pdf"><span style="mso-bookmark:_Toc23346647">JDV_J07-XdsTypeCode-CISIS</span></a><span style="mso-bookmark:_Toc23346647"> d</span><span style="mso-bookmark:_Toc23346647"><span style="mso-bidi-font-family:Arial;color:black">e la Nomenclature des Objets
  de Santé (NOS). <o:p></o:p></span></span></p>
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647">Par exemple&nbsp;: 11502-2</span></p>
  </td>
  
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">IS<o:p></o:p></span></span></p>
  </td>
  
  <td width="180" valign="top" style="width:134.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">TXA-3<o:p></o:p></span></span></p>
  </td>
  
  <td width="350" valign="top" style="width:262.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647">Document Content <span class="SpellE">Presentation</span></span></p>
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647"><span style="color:#0070C0">TEXT</span></span></p>
  </td>
  
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">ID<o:p></o:p></span></span></p>
  </td>
  
  <td width="180" valign="top" style="width:134.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:4">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">TXA-12 <i>(Note 1)</i><o:p></o:p></span></span></p>
  </td>
  
  <td width="350" valign="top" style="width:262.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647">Unique document <span class="SpellE">number</span></span></p>
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647">Si <span class="SpellE"><span style="color:black">ClinicalDocument</span></span><span style="color:black">/<span class="SpellE">id@extension</span> est renseigné :</span></span></p>
  <p class="MsoNormal" align="left" style="margin-left:35.4pt;text-align:left"><span style="mso-bookmark:_Toc23346647"><span style="mso-spacerun:yes">&nbsp;</span><span class="GramE">ex</span>&nbsp;: 58132^^1.2.250.2345.3245.13^ISO</span></p>
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647">Si <span class="SpellE"><span style="color:black">ClinicalDocument</span></span><span style="color:black">/<span class="SpellE">id@extension</span> n’est pas
  renseigné :</span></span></p>
  <p class="MsoNormal" align="left" style="margin-left:35.4pt;text-align:left"><span style="mso-bookmark:_Toc23346647"><span style="mso-spacerun:yes">&nbsp;</span><span class="GramE">ex</span>&nbsp;: 1.2.250.2345.3245.13.58132</span></p>
  </td>
  
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">EI<o:p></o:p></span></span></p>
  </td>
  
  <td width="180" valign="top" style="width:134.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:5">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">TXA-13 <i>(Note 1)</i><o:p></o:p></span></span></p>
  </td>
  
  <td width="350" valign="top" style="width:262.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647">Parent document <span class="SpellE">number</span></span></p>
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647">Si <span class="SpellE"><span style="color:black">ClinicalDocument</span></span><span style="color:black">/<span class="SpellE">id@extension</span> est renseigné :</span></span></p>
  <p class="MsoNormal" align="left" style="margin-left:35.4pt;text-align:left"><span style="mso-bookmark:_Toc23346647"><span style="mso-spacerun:yes">&nbsp;</span><span class="GramE">ex</span>&nbsp;: 58131^^1.2.250.2345.3245.13^ISO</span></p>
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647">Si <span class="SpellE"><span style="color:black">ClinicalDocument</span></span><span style="color:black">/<span class="SpellE">id@extension</span> n’est pas
  renseigné :</span></span></p>
  <p class="MsoNormal" align="left" style="margin-left:35.4pt;text-align:left"><span style="mso-bookmark:_Toc23346647"><span style="mso-spacerun:yes">&nbsp;</span><span class="GramE">ex</span>&nbsp;: 1.2.250.2345.3245.13.58131 </span></p>
  </td>
  
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">EI<o:p></o:p></span></span></p>
  </td>
  
  <td width="180" valign="top" style="width:134.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">C (Requis dans le cas d’une demande de remplacement)<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:6;mso-yfti-lastrow:yes">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">TXA-17<o:p></o:p></span></span></p>
  </td>
  
  <td width="350" valign="top" style="width:262.25pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647">Document <span class="SpellE">completion</span> <span class="SpellE">status</span> dont la valeur est à prendre dans la table HL7
  0271</span></p>
  <p class="MsoNormal" align="left" style="text-align:left"><span style="mso-bookmark:
  _Toc23346647"><span style="color:#0070C0">AU</span></span></p>
  </td>
  
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">ID<o:p></o:p></span></span></p>
  </td>
  
  <td width="180" valign="top" style="width:134.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="color:black">R<o:p></o:p></span></span></p>
  </td>
  
 </tr>
</tbody></table>
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

#### Les données concernant la demande de traitement sur le document
##### Le groupe de segments OBXNTE portant le document CDA

Le message HL7 MDM contient un premier groupe OBXNTE composé :

-   d'un segment OBX contenant un document encodé en Base64 dont le type
    MIME est précisé en OBX-5.2, il peut s'agir d'un document CDA-R2
    Niv1 ou d'un CDA-R2 Niv3,

-   d'un segment PRT requis, pré-adopté de HL7v2.9, véhiculant les
    informations sur l'expéditeur du courriel MSSanté,

-   d'un segment PRT requis si connu, pré-adopté de HL7v2.9, véhiculant
    les informations sur le destinataire du courriel MSSanté,

-   d'un segment PRT optionnel, pré-adopté de HL7v2.9, permettant de
    renseigner l'adresse mail sur laquelle le destinataire peut
    répondre.

Les champs des segments PRT doivent être renseignés conformément aux
spécifications [« Contraintes sur les types de données HL7 v2.5
applicables aux profils d'intégration du cadre technique IT
Infrastructure dans le périmètre d'IHE France » release 1.8](https://old.interopsante.org/offres/doc_inline_src/412/IHE_France_Constraints_on_HL7_data_types_for_ITI_V1.8.pdf).

Les tableaux suivants listent l'ensemble des **segments et des champs à
renseigner obligatoirement**, dans l'ordre indiqué, à l'exception du
dernier segment PRT permettant de préciser l'adresse mail de réponse
(qui est optionnel). Seuls les segments et les champs indiqués dans les
tableaux suivants sont à renseigner dans le message MDM :
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="652" style="width:488.8pt;border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes">
  <td width="652" colspan="3" valign="top" style="width:488.8pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#E5E5E5;mso-shading:windowtext;
  mso-pattern:gray-10 auto;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Composition du groupe
  OBXNTE&nbsp;: Usage&nbsp;= <span class="SpellE">Required</span> /
  Cardinalité&nbsp;= [<span class="GramE">1..</span>1]<o:p></o:p></span></b></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  background:#E5E5E5;mso-shading:windowtext;mso-pattern:gray-10 auto;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Elément requis&nbsp;:<o:p></o:p></span></b></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#E5E5E5;mso-shading:windowtext;
  mso-pattern:gray-10 auto;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Description&nbsp;: <o:p></o:p></span></b></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#E5E5E5;mso-shading:windowtext;
  mso-pattern:gray-10 auto;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Valeur&nbsp;: <o:p></o:p></span></b></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Segment OBX<o:p></o:p></span></b></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Observation/<span class="SpellE">Result</span><o:p></o:p></span></b></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Contient un document au format
  CDA-R2<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">OBX-1<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Set Id - <span class="SpellE">Obx</span><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  mso-bidi-font-weight:bold">Numéro de séquence du segment<o:p></o:p></span></span></p>
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">1<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:4">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">OBX-2&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Value Type<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">ED </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold">(<span class="SpellE">Encapsuled</span> Data)<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:5">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">OBX-3&nbsp;= OBR-4<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Observation Identifier <o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p>&nbsp;</o:p></span></b></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:6">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; OBX-3.1&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Code du Document<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" rowspan="2" valign="top" style="width:210.1pt;border-top:none;
  border-left:none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Utiliser le </span></span><a href="https://mos.esante.gouv.fr/NOS/JDV_J07-XdsTypeCode-CISIS/JDV_J07-XdsTypeCode-CISIS.pdf"><span style="mso-bookmark:_Toc23346647">JDV_J07-XdsTypeCode-CISIS</span></a><span style="mso-bookmark:_Toc23346647"><span style="mso-bidi-font-family:Arial;
  color:black"> </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">de la Nomenclature des Objets de Santé (NOS)</span></span><span style="mso-bookmark:_Toc23346647"><span style="mso-bidi-font-family:Arial;
  color:black"> </span></span><span style="mso-bookmark:_Toc23346647"><sup><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></sup></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:7">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; OBX-3.2&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Libellé du Document<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:8">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt;OBX-3.3<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Système de codage dont est issu le
  code<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">LN </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;mso-bidi-font-weight:bold">ou <span style="color:#0070C0">TRE_A05 </span><span style="color:black">en fonction de
  l’appartenance du code à l’un de ces systèmes de codage.</span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:9">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">OBX-5&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Observation Value<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:10">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; OBX-5.1<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Source Application<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:11">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; OBX-5.2<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Type<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="GramE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0">text</span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:12">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; OBX-5.3<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Data <span class="SpellE">Subtype</span><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Le champ prend la valeur </span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0">XML</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">. <o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:13">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; OBX-5.4<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Encoding</span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0">Base64</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:14">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; OBX-5.5<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Data<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Intégrer le document CDA<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:15">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">OBX-11<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Observation <span class="SpellE">Result</span>
  Status<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Statut du document pris dans la table HL7 0085 (Observation <span class="SpellE">Result</span> Status Codes <span class="SpellE">Interpretation</span>)<o:p></o:p></span></span></p>
  <p class="MsoListParagraphCxSpFirst" style="margin-bottom:8.0pt;mso-add-space:
  auto;text-indent:-18.0pt;line-height:107%;mso-list:l29 level1 lfo12"><span style="mso-bookmark:_Toc23346647"><!--[if !supportLists]--><span style="font-size:9.0pt;line-height:107%;font-family:Symbol;mso-fareast-font-family:
  Symbol;mso-bidi-font-family:Symbol;color:black"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span></span><!--[endif]--><span style="font-size:9.0pt;line-height:107%;mso-bidi-font-family:Arial;
  color:#0070C0">F&nbsp;</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:107%;mso-bidi-font-family:Arial;
  color:black">: Document validé<o:p></o:p></span></span></p>
  <p class="MsoListParagraphCxSpMiddle" style="margin-bottom:8.0pt;mso-add-space:
  auto;text-indent:-18.0pt;line-height:107%;mso-list:l29 level1 lfo12"><span style="mso-bookmark:_Toc23346647"><!--[if !supportLists]--><span style="font-size:9.0pt;line-height:107%;font-family:Symbol;mso-fareast-font-family:
  Symbol;mso-bidi-font-family:Symbol;color:black"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span></span><!--[endif]--><span style="font-size:9.0pt;line-height:107%;mso-bidi-font-family:Arial;
  color:#0070C0">D&nbsp;</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:107%;mso-bidi-font-family:Arial;
  color:black">: Document à supprimer<o:p></o:p></span></span></p>
  <p class="MsoListParagraphCxSpLast" style="text-indent:-18.0pt;mso-list:l29 level1 lfo12"><span style="mso-bookmark:_Toc23346647"><!--[if !supportLists]--><span style="font-size:9.0pt;line-height:115%;font-family:Symbol;mso-fareast-font-family:
  Symbol;mso-bidi-font-family:Symbol;color:black"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span></span><!--[endif]--><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0">C&nbsp;</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">: Remplacement du Document<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:16">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Segment PRT (Requis)</span></b></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Participation Information&nbsp;<br>
  <span style="mso-bidi-font-weight:bold">Expéditeur</span></span></b></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Ce segment contient les informations
  de l’expéditeur à l’origine de la demande de traitement sur le document.</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:17">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-2&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Action Code<span style="mso-bidi-font-weight:bold"><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">UC </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold">(<span class="SpellE">Unchanged</span>)<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:18">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-4&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Participation </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-ansi-language:EN-US;mso-bidi-font-weight:bold"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:19">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-4.1<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Code&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">SB </span></span><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0;mso-ansi-language:
  EN-US;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:20">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-4.2<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Libellé du code<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-ansi-language:EN-US;mso-bidi-font-weight:bold">Send by<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:21">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-4.3<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Name Of Coding System<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="GramE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0">participation</span></span></span><span style="mso-bookmark:
  _Toc23346647"><span lang="EN-US" style="font-size:9.0pt;line-height:115%;
  mso-bidi-font-family:Arial;color:#0070C0;mso-ansi-language:EN-US;mso-bidi-font-weight:
  bold"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:22">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-5 (Requis si connu)<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Participation Person<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Ce champ est requis si connu si
  l’expéditeur est un professionnel de santé (Note 1).<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:23">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-5.1 (Requis si connu)<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">ID <span class="SpellE">number</span><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Identifiant du professionnel de santé expéditeur<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:24">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-5.2 (Requis si connu)<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Family Name<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Nom d’exercice de l’expéditeur<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:25">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-5.3 (Requis si connu)<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Given</span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"> Name<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Prénom d’exercice de l’expéditeur<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:26">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">&gt; PRT-5.9 (<span style="mso-bidi-font-weight:bold">Requis si
  connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Assigning</span></span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"> <span class="SpellE">Authority</span><span style="mso-bidi-font-weight:bold"><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Autorité d’affectation de
  l’identifiant de l’expéditeur&nbsp;<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:27">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-5.13 (Conditionnel)</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Identifier Type Code</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Le type d’identifiant (</span></span><a href="http://www.interopsante.org/offres/doc_inline_src/412/IHE_France_Constraints_on_HL7_data_types_for_ITI_v.1.7.3.pdf"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;mso-bidi-font-weight:bold">Table 0203 – <span class="SpellE">Interop’Santé</span></span></span></a><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">) est requis lorsque le PRT-5.1
  est renseigné<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:28">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-8 (Requis si connu)</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black">Participation
  <span class="SpellE">Organization</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Ce champ est requis si connu si
  l’expéditeur est une organisation (Note 1).<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:29">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-8.1 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Requis si connu)</span><o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black">OrganizationName</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Nom de l’organisation <o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:30">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-8.6 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Requis si connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black">Assigning</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:
  9.0pt;line-height:115%;color:black"> <span class="SpellE">Authority</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Autorité d’affectation de
  l’identifiant de l’organisation expéditrice du document<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:31">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-8.7 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Requis si connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black">Identifier
  Type Code<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Type d’identifiant (</span></span><a href="http://www.interopsante.org/offres/doc_inline_src/412/IHE_France_Constraints_on_HL7_data_types_for_ITI_v.1.7.3.pdf"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;mso-bidi-font-weight:bold">Table 0203 – <span class="SpellE">Interop’Santé</span></span></span></a><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">)<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:32">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-8.10 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Requis si connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black">Organization</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:
  9.0pt;line-height:115%;color:black"> <span class="SpellE">number</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Identifiant de l’organisation
  expéditrice du document<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:33">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-10 (Conditionnel)</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black">Participation
  <span class="SpellE">Device</span></span></span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Ce champ est requis si l’expéditeur
  est une application.<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:34">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-10.1</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black">Entity</span></span></span></span><span style="mso-bookmark:
  _Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black"> Identifier</span></span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Identifiant de l’application<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:35">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-15&nbsp;(Requis)</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black;
  mso-bidi-font-weight:bold">Participant <span class="SpellE">Telecommunication</span>
  <span class="SpellE">Address</span></span></span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:36">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-15.3<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black">Telecommunication</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:
  9.0pt;line-height:115%;color:black"> Equipment Type<span style="mso-bidi-font-weight:
  bold"><o:p></o:p></span></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0">X.400 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial">(X</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%">.400 <span class="GramE">email</span> <span class="SpellE">address</span>)</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:#0070C0;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:37">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-15.4<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black">Communication
  <span class="SpellE">Address</span><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Intégrer l’adresse <span class="GramE">mail</span> de l’expéditeur<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:38">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Segment PRT (Requis si connu)</span></b></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Participation Information&nbsp;<br>
  <span class="cx-body">Destinataire</span></span></b></span><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:
  9.0pt;line-height:115%;color:black"><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Contient les informations du
  destinataire initial du courriel MSSanté. Cf (Note 1), (Note 2).</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:39">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-2&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Action Code<span style="mso-bidi-font-weight:bold"><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">UC </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold">(<span class="SpellE">Unchanged</span>)<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:40">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-4&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Participation </span><span class="cx-body"><span style="color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-ansi-language:EN-US;mso-bidi-font-weight:bold"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:41">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-4.1<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Code&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-ansi-language:EN-US;mso-bidi-font-weight:bold">RCT<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:42">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-4.2<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Libellé du code<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0">Result</span></span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0"> Copies To</span></span><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-ansi-language:EN-US;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:43">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-4.3<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Name Of Coding System<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="GramE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0">participation</span></span></span><span style="mso-bookmark:
  _Toc23346647"><span lang="EN-US" style="font-size:9.0pt;line-height:115%;
  mso-bidi-font-family:Arial;color:#0070C0;mso-ansi-language:EN-US;mso-bidi-font-weight:
  bold"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:44">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-5 (Requis si connu)<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Participation Person<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Ce champ est requis si connu si le
  destinataire initial du courriel est un PS<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:45">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-5.1 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Requis si connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">ID <span class="SpellE">number</span><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Identifiant du destinataire<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:46">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-5.2 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Requis si connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Family Name<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Nom d’exercice du destinataire<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:47">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-5.3 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Requis si connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Given</span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"> Name<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Prénom d’exercice du destinataire<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:48">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">&gt; PRT-5.9 (<span style="mso-bidi-font-weight:bold">Requis si
  connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Assigning</span></span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"> <span class="SpellE">Authority</span><span style="mso-bidi-font-weight:bold"><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Autorité d’affectation de
  l’identifiant du destinataire<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:49">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-5.13 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Conditionnel)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Identifier Type Code<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Le type d’identifiant (</span></span><a href="http://www.interopsante.org/offres/doc_inline_src/412/IHE_France_Constraints_on_HL7_data_types_for_ITI_v.1.7.3.pdf"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;mso-bidi-font-weight:bold">Table 0203 – <span class="SpellE">Interop’Santé</span></span></span></a><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">) est requis lorsque le PRT-5.1
  est renseigné<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:50">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-8 (Requis si connu)<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black">Participation
  <span class="SpellE">Organization</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Ce champ permet de faciliter le
  traitement du document dans la bonne organisation au niveau du système CONSOMMATEUR
  (service, UF, pôle…). Cf (Note 3).<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:51">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-8.1 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Requis si connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black">OrganizationName</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Nom du destinataire<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:52">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-8.6 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Requis si connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black">Assigning</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:
  9.0pt;line-height:115%;color:black"> <span class="SpellE">Authority</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Autorité d’affectation de
  l’identifiant du destinataire<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:53">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-8.7 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Requis si connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black">Identifier
  Type Code</span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Type d’identifiant (</span></span><a href="http://www.interopsante.org/offres/doc_inline_src/412/IHE_France_Constraints_on_HL7_data_types_for_ITI_v.1.7.3.pdf"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;mso-bidi-font-weight:bold">Table 0203 – <span class="SpellE">Interop’Santé</span></span></span></a><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">)<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:54">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-8.10 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">(<span style="mso-bidi-font-weight:
  bold">Requis si connu)<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black">Organization</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:
  9.0pt;line-height:115%;color:black"> <span class="SpellE">number</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Identifiant du destinataire<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:55">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-15&nbsp;(Requis)<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black;
  mso-bidi-font-weight:bold">Participant <span class="SpellE">Telecommunication</span>
  <span class="SpellE">Address</span></span></span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:56">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-15.3<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black;mso-bidi-font-weight:bold">Telecommunication</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:
  9.0pt;line-height:115%;color:black;mso-bidi-font-weight:bold"> Equipment Type<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">X.400 </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;mso-bidi-font-weight:bold">(X</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-weight:bold">.400 <span class="GramE">email</span> <span class="SpellE">address</span>)</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:57">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-15.4<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black">Communication
  <span class="SpellE">Address</span><span style="mso-bidi-font-weight:bold"><o:p></o:p></span></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Intégrer l’adresse MSSanté du destinataire<span style="mso-bidi-font-weight:bold"><o:p></o:p></span></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:58">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Segment PRT (segment optionnel)</span></b></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Participation Information<br>
  <span class="cx-body">adresse de réponse</span></span></b></span><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><b><span style="font-size:9.0pt;line-height:115%;color:black"><o:p></o:p></span></b></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Ce segment optionnel permet d’indiquer
  l’adresse <span class="GramE">mail</span> sur laquelle le destinataire peut
  répondre. </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:59">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-2&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black;
  mso-bidi-font-weight:bold">Action Code</span></span></span><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:
  9.0pt;line-height:115%;color:black"><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">UC </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold">(<span class="SpellE">Unchanged</span>)</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:60">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-4&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Participation </span></span><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:
  9.0pt;line-height:115%;color:black"><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:61">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-4.1<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Code&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">REPLY</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;mso-ansi-language:EN-US;mso-bidi-font-weight:
  bold"> </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:62">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-4.2<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Libellé du code<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0">Reply</span></span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0"> To<span style="mso-bidi-font-weight:bold"><o:p></o:p></span></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:63">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-4.3<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Name Of Coding System<o:p></o:p></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="GramE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0">participation</span></span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:64">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">PRT-15&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black;
  mso-bidi-font-weight:bold">Participant <span class="SpellE">Telecommunication</span>
  <span class="SpellE">Address</span></span></span></span><span style="mso-bookmark:
  _Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black"><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:65">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-15.3<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="SpellE"><span class="cx-body"><span style="font-size:9.0pt;line-height:
  115%;color:black">Telecommunication</span></span></span></span><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:
  9.0pt;line-height:115%;color:black"> Equipment Type<o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-ansi-language:EN-US">X.400 </span></span><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;mso-ansi-language:EN-US">(X</span></span><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="font-size:9.0pt;
  line-height:115%;mso-ansi-language:EN-US">.400 email address)</span></span><span style="mso-bookmark:_Toc23346647"><span lang="EN-US" style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:black;mso-ansi-language:
  EN-US"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:66;mso-yfti-lastrow:yes">
  <td width="192" valign="top" style="width:144.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; PRT-15.4<o:p></o:p></span></span></p>
  </td>
  
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span class="cx-body"><span style="font-size:9.0pt;line-height:115%;color:black">Communication
  <span class="SpellE">Address</span><o:p></o:p></span></span></span></p>
  </td>
  
  <td width="280" valign="top" style="width:210.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Intégrer l’adresse <span class="GramE">mail</span> de réponse<o:p></o:p></span></span></p>
  </td>
  
 </tr>
</tbody></table>
_**Note 1 :** le renseignement des informations concernant l’identification de l’expéditeur/destinataire est conditionné à la capacité du GESTIONNAIRE à interroger l’annuaire de l’établissement._

_**Note 2 :** en cas de transfert du courriel original au niveau de l’établissement destinataire, il n’est pas certain que l’acteur GESTIONNAIRE puisse récupérer l’information concernant le destinataire initial du courriel. Cette information peut être utilisée pour notifier au niveau du système CONSOMMATEUR, le PS ou le service clinique concerné par le courriel (organisation) du résultat du traitement réalisé sur le document par le système CONSOMMATEUR._

_**Note 3 :** dans la configuration où le GESTIONNAIRE est en capacité de maintenir une table de correspondance entre une BAL et une organisation correspondante (service clinique, UF, pôle…), le champ PRT-8 permet de préciser l’organisation de l’établissement concerné par la demande de traitement sur le document au niveau du CONSOMMATEUR. Dans le cas où le GESTIONNAIRE n’est pas en capacité de maintenir cette table de correspondance, le système CONSOMMATEUR peut prévoir un paramétrage pour associer une organisation de l’établissement (service clinique, UF, pôle…) à une BAL afin de réaliser le traitement sur le document dans la bonne organisation._

##### Le groupe de segments portant les informations du courriel MSSanté

<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="680" style="width:510.05pt;border-collapse:collapse;border:none;mso-border-alt:
 solid windowtext .5pt;mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:8.8pt">
  <td width="680" colspan="3" valign="top" style="width:510.05pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;
  height:8.8pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Composition du groupe
  OBXNTE&nbsp;: Usage&nbsp;= <span class="SpellE">Required</span> /
  Cardinalité&nbsp;= <s>[</s><span class="GramE">1..</span>1]<o:p></o:p></span></b></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="156" valign="top" style="width:116.7pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  background:#D9D9D9;mso-background-themecolor:background1;mso-background-themeshade:
  217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Elément requis&nbsp;:<o:p></o:p></span></b></span></p>
  </td>
  
  <td width="163" valign="top" style="width:122.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Description&nbsp;: <o:p></o:p></span></b></span></p>
  </td>
  
  <td width="361" valign="top" style="width:270.9pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Valeur&nbsp;: <o:p></o:p></span></b></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="156" valign="top" style="width:116.7pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Segment OBX<o:p></o:p></span></b></span></p>
  </td>
  
  <td width="163" valign="top" style="width:122.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black">Observation/<span class="SpellE">Result</span><o:p></o:p></span></b></span></p>
  </td>
  
  <td width="361" valign="top" style="width:270.9pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Contient les informations du courriel
  MSSanté dont a été extrait le document <o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="156" valign="top" style="width:116.7pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">OBX-1<o:p></o:p></span></span></p>
  </td>
  
  <td width="163" valign="top" style="width:122.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Set Id - <span class="SpellE">Obx</span><o:p></o:p></span></span></p>
  </td>
  
  <td width="361" valign="top" style="width:270.9pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  mso-bidi-font-weight:bold">Numéro de séquence du segment<o:p></o:p></span></span></p>
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">2<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:4">
  <td width="156" style="width:116.7pt;border:solid windowtext 1.0pt;border-top:
  none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">OBX-2<o:p></o:p></span></span></p>
  </td>
  
  <td width="163" valign="top" style="width:122.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Value Type<o:p></o:p></span></span></p>
  </td>
  
  <td width="361" valign="top" style="width:270.9pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0;mso-bidi-font-weight:bold">ED </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-bidi-font-weight:bold">(<span class="SpellE">Encapsulated</span> Data)</span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:5">
  <td width="156" valign="top" style="width:116.7pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-themecolor:text1;mso-bidi-font-weight:bold">OBX-3&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="163" valign="top" style="width:122.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-themecolor:text1;mso-bidi-font-weight:bold">Observation
  Identifier <o:p></o:p></span></span></p>
  </td>
  
  <td width="361" valign="top" style="width:270.9pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-themecolor:text1;mso-bidi-font-weight:bold"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:6">
  <td width="156" valign="top" style="width:116.7pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; OBX-3.1&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span></span></span><span style="mso-bookmark:
  _Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-themecolor:text1;mso-bidi-font-weight:bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="163" valign="top" style="width:122.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Identifier </span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:
  115%;mso-bidi-font-family:Arial;color:black;mso-themecolor:text1;mso-bidi-font-weight:
  bold"><o:p></o:p></span></span></p>
  </td>
  
  <td width="361" valign="top" style="width:270.9pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-themecolor:text1;mso-bidi-font-weight:bold">Identifiant
  unique du courriel correspondant à l’élément Message-ID de l’entête du
  courriel MSSanté<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:7">
  <td width="156" valign="top" style="width:116.7pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">&gt; OBX-3.2&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></span></p>
  </td>
  
  <td width="163" valign="top" style="width:122.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Text<o:p></o:p></span></span></p>
  </td>
  
  <td width="361" valign="top" style="width:270.9pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Objet du courriel<o:p></o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:8">
  <td width="156" valign="top" style="width:116.7pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">OBX-4<span style="mso-spacerun:yes">&nbsp;
  </span><o:p></o:p></span></span></p>
  </td>
  
  <td width="163" valign="top" style="width:122.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Observation <span class="SpellE">Sub</span>-id<o:p></o:p></span></span></p>
  </td>
  
  <td width="361" valign="top" style="width:270.9pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt"><span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:9">
  <td width="156" valign="top" style="width:116.7pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">OBX-5&nbsp;<o:p></o:p></span></span></p>
  </td>
  
  <td width="163" valign="top" style="width:122.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Observation Value<o:p></o:p></span></span></p>
  </td>
  
  <td width="361" valign="top" style="width:270.9pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Contenu du courriel codé en base 64<o:p></o:p></span></span></p>
  <span style="mso-bookmark:_Toc23346647"></span>
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p>&nbsp;</o:p></span></span></p>
  </td>
  
 </tr>
 <tr style="mso-yfti-irow:10;mso-yfti-lastrow:yes">
  <td width="156" valign="top" style="width:116.7pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">OBX-11<o:p></o:p></span></span></p>
  </td>
  
  <td width="163" valign="top" style="width:122.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">Observation <span class="SpellE">Result</span>
  Status<o:p></o:p></span></span></p>
  </td>
  
  <td width="361" valign="top" style="width:270.9pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Valeur fixée à «</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0">&nbsp;F&nbsp;</span></span><span style="mso-bookmark:_Toc23346647"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">»<o:p></o:p></span></span></p>
  </td>
  
 </tr>
</tbody></table>

##### Groupes OBXNTE portant les métadonnées MSSanté

Cette section présente uniquement les métadonnées de restriction indispensables aux échanges avec la MSSanté. Ces groupes sont conformes à ceux définis dans le volet « Transmission de documents CDA en HL7v2 » version 2.1

Les métadonnées peuvent être valorisées avec Y ou N suivant qu’elles sont activées ou non au moment de la validation du document.

Ces métadonnées sont requises et doivent apparaître dans le message MDM dans l’ordre présenté ci-dessous.

Pour l’ensemble des OBX listés dans cette section, le champ OBX-3 prend ses valeurs dans la [table « MetaDMP/MSS »](meta-dmp-mss.html). Le champ OBX-11 étant requis par le standard HL7v2, la valeur de ce champ est arbitrairement fixée à « F ».

###### Document Masqué aux professionnels de Santé
Cet OBX permet au Consommateur de vérifier que le document n’est pas masqué aux professionnels de santé.
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="652" style="width:488.8pt;border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes">
  <td width="652" colspan="3" valign="top" style="width:488.8pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Composition du groupe OBSERVATION/OBXNTE&nbsp;: Usage&nbsp;= <span class="SpellE">Required</span> / Cardinalité&nbsp;= [<span class="GramE">1..</span>1]<o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  background:#D9D9D9;mso-background-themecolor:background1;mso-background-themeshade:
  217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Elément requis&nbsp;:<o:p></o:p></span></b></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Description&nbsp;: <o:p></o:p></span></b></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Valeur&nbsp;: <o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Segment OBX<o:p></o:p></span></b></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Observation/<span class="SpellE">Result</span><o:p></o:p></span></b></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-1<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Set Id - <span class="SpellE">Obx</span><o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;mso-bidi-font-weight:bold">Numéro
  de séquence du segment<o:p></o:p></span></p>
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0;mso-bidi-font-weight:
  bold">3<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-2<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Value Type<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0;mso-bidi-font-weight:bold">CWE </span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">(<span class="SpellE">Coded</span> <span class="SpellE">with</span> Exceptions)</span><b style="mso-bidi-font-weight:
  normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-3<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Observation Identifier <o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.1&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Code&nbsp;:<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0">MASQUE_PS<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.2&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Libellé&nbsp;:<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0">Masqué aux professionnels de Santé<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.3&nbsp;:<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Name of Coding system<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span class="SpellE"><span style="font-size:9.0pt;
  line-height:115%;color:#0070C0">MetaDMPMSS</span></span><span style="font-size:9.0pt;line-height:115%;color:#4472C4;mso-themecolor:accent5"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-5<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Observation Value<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-5.1<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Code&nbsp;: <o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Table HL7 : 0136&nbsp;:</span><span style="font-size:8.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></p>
  <p class="MsoListParagraph" style="margin-top:0cm;margin-right:0cm;margin-bottom:
  0cm;margin-left:18.0pt;mso-add-space:auto;text-indent:-18.0pt;line-height:
  normal;mso-list:l1 level1 lfo15"><!--[if !supportLists]--><span style="font-size:
  9.0pt;font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
  Symbol;color:black"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  </span></span></span><!--[endif]--><span style="font-size:9.0pt;mso-bidi-font-family:
  Arial;color:#0070C0">N </span><span style="font-size:9.0pt;mso-bidi-font-family:
  Arial;color:black">(No)&nbsp;</span><span style="font-size:9.0pt;font-family:
  Wingdings;mso-fareast-font-family:Wingdings;mso-bidi-font-family:Wingdings;
  color:black">à</span><span style="font-size:9.0pt;mso-bidi-font-family:Arial;
  color:black"> MASQUE_PS non Actif<o:p></o:p></span></p>
    <p class="MsoListParagraph" style="margin-top:0cm;margin-right:0cm;margin-bottom:
  0cm;margin-left:18.0pt;mso-add-space:auto;text-indent:-18.0pt;line-height:
  normal;mso-list:l1 level1 lfo15"><!--[if !supportLists]--><span style="font-size:
  9.0pt;font-family:Symbol;mso-fareast-font-family:Symbol;mso-bidi-font-family:
  Symbol;color:black"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  </span></span></span><!--[endif]--><span style="font-size:9.0pt;mso-bidi-font-family:
  Arial;color:#0070C0">Y </span><span style="font-size:9.0pt;mso-bidi-font-family:
  Arial;color:black">(Yes)&nbsp;</span><span style="font-size:9.0pt;font-family:
  Wingdings;mso-fareast-font-family:Wingdings;mso-bidi-font-family:Wingdings;
  color:black">à</span><span style="font-size:9.0pt;mso-bidi-font-family:Arial;
  color:black"> MASQUE_PS Actif<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-5.3<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Name Of Coding System<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="Default" style="text-align:justify"><span class="SpellE"><span class="GramE"><span style="font-size:9.0pt;font-family:&quot;Arial&quot;,sans-serif;
  color:#0070C0">expandedYes</span></span><span style="font-size:9.0pt;
  font-family:&quot;Arial&quot;,sans-serif;color:#0070C0">-NoIndicator</span></span><span style="font-size:9.0pt;font-family:&quot;Arial&quot;,sans-serif;color:#0070C0"> </span><span style="font-size:9.0pt;mso-bidi-font-family:Arial"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;mso-yfti-lastrow:yes">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-11<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Observation <span class="SpellE">Result</span>
  Status<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Valeur fixée à «</span><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0">&nbsp;F&nbsp;</span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">»&nbsp;<o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

###### Document Non visible par le patient
Cet OBX permet d’informer le Consommateur que le document est masqué ou non au patient.
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="652" style="width:488.8pt;border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes">
  <td width="652" colspan="3" valign="top" style="width:488.8pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Composition du groupe OBSERVATION/OBXNTE&nbsp;: Usage&nbsp;= <span class="SpellE">Required</span> / Cardinalité&nbsp;= [<span class="GramE">1..</span>1]<o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  background:#D9D9D9;mso-background-themecolor:background1;mso-background-themeshade:
  217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Elément requis&nbsp;:<o:p></o:p></span></b></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Description&nbsp;: <o:p></o:p></span></b></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Valeur&nbsp;: <o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Segment OBX</span></b><u><span style="color:black"><o:p></o:p></span></u></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Observation/<span class="SpellE">Result</span><o:p></o:p></span></b></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-1<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Set Id - <span class="SpellE">Obx</span><o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;mso-bidi-font-weight:bold">Numéro
  de séquence du segment<o:p></o:p></span></p>
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0;mso-bidi-font-weight:
  bold">4<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-2<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Value Type<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0;mso-bidi-font-weight:bold">CWE </span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">(<span class="SpellE">Coded</span> <span class="SpellE">with</span> Exceptions)</span><b style="mso-bidi-font-weight:
  normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-3<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Observation Identifier <o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.1&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Code&nbsp;: <o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0">INVISIBLE_PATIENT<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.2&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Libellé&nbsp;:<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0">Document Non Visible par le patient<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.3&nbsp;:<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Name of Coding system<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span class="SpellE"><span style="font-size:9.0pt;
  line-height:115%;color:#0070C0">MetaDMPMSS</span></span><span style="font-size:9.0pt;line-height:115%;color:#4472C4;mso-themecolor:accent5"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-5<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Observation Value<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-5.1<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Code&nbsp;: <o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Table HL7 : 0136&nbsp;:</span><span style="font-size:8.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></p>
  <p class="MsoListParagraphCxSpFirst" style="margin-top:0cm;margin-right:0cm;
  margin-bottom:0cm;margin-left:18.0pt;mso-add-space:auto;text-indent:-18.0pt;
  line-height:normal;mso-list:l1 level1 lfo15"><!--[if !supportLists]--><span style="font-size:9.0pt;font-family:Symbol;mso-fareast-font-family:Symbol;
  mso-bidi-font-family:Symbol;color:black"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span></span><!--[endif]--><span style="font-size:9.0pt;mso-bidi-font-family:Arial;color:#0070C0">Y</span><span style="font-size:9.0pt;mso-bidi-font-family:Arial;color:black"> (YES) </span><span style="font-size:9.0pt;font-family:Wingdings;mso-fareast-font-family:Wingdings;
  mso-bidi-font-family:Wingdings;color:black">à</span><span style="font-size:
  9.0pt;mso-bidi-font-family:Arial;color:black"> INVISIBLE_PATIENT actif<o:p></o:p></span></p>
  <p class="MsoListParagraphCxSpLast" style="margin-top:0cm;margin-right:0cm;
  margin-bottom:0cm;margin-left:18.0pt;mso-add-space:auto;text-indent:-18.0pt;
  line-height:normal;mso-list:l1 level1 lfo15"><!--[if !supportLists]--><span style="font-size:9.0pt;font-family:Symbol;mso-fareast-font-family:Symbol;
  mso-bidi-font-family:Symbol;color:black"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span></span><!--[endif]--><span style="font-size:9.0pt;mso-bidi-font-family:Arial;color:#0070C0">N</span><span style="font-size:9.0pt;mso-bidi-font-family:Arial;color:black"> (No) </span><span style="font-size:9.0pt;font-family:Wingdings;mso-fareast-font-family:Wingdings;
  mso-bidi-font-family:Wingdings;color:black">à</span><span style="font-size:
  9.0pt;mso-bidi-font-family:Arial;color:black"> INVISIBLE_PATIENT non actif<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-5.3<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Name Of Coding System<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span class="SpellE"><span class="GramE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0">expandedYes</span></span><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0">-NoIndicator</span></span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;mso-yfti-lastrow:yes">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-11<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Observation <span class="SpellE">Result</span>
  Status<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Valeur fixée à «&nbsp;</span><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0">F</span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">&nbsp;»&nbsp;<o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

###### Document Non visible par les représentants légaux du patient
Cet OBX permet d’informer le Consommateur que le document est masqué ou non aux représentants légaux du patient.
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="652" style="width:488.8pt;border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes">
  <td width="652" colspan="3" valign="top" style="width:488.8pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Composition du groupe OBSERVATION/OBXNTE&nbsp;: Usage&nbsp;= <span class="SpellE">Required</span> / Cardinalité&nbsp;= [<span class="GramE">1..</span>1]<o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  background:#D9D9D9;mso-background-themecolor:background1;mso-background-themeshade:
  217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Elément requis&nbsp;:<o:p></o:p></span></b></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Description&nbsp;: <o:p></o:p></span></b></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Valeur&nbsp;: <o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Segment OBX<o:p></o:p></span></b></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Observation/<span class="SpellE">Result</span><o:p></o:p></span></b></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-1<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Set Id - <span class="SpellE">Obx</span><o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;mso-bidi-font-weight:bold">Numéro
  de séquence du segment<o:p></o:p></span></p>
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0;mso-bidi-font-weight:
  bold">5<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-2<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Value Type<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0;mso-bidi-font-weight:bold">CWE </span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">(<span class="SpellE">Coded</span> <span class="SpellE">with</span> Exceptions)</span><b style="mso-bidi-font-weight:
  normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-3<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Observation Identifier <o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.1&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Code&nbsp;: <o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0">INVISIBLE_ REP_LEGAUX<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.2&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Libellé&nbsp;:<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0">Non visible par les représentants Légaux du patient<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.3&nbsp;:<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Name of Coding system<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span class="SpellE"><span style="font-size:9.0pt;
  line-height:115%;color:#0070C0">MetaDMPMSS</span></span><span style="font-size:9.0pt;line-height:115%;color:#4472C4;mso-themecolor:accent5"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-5<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Observation Value<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-5.1<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Code&nbsp;: <o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Table HL7 : 0136&nbsp;:</span><span style="font-size:8.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></p>
  <p class="MsoListParagraphCxSpFirst" align="left" style="margin-top:0cm;
  margin-right:0cm;margin-bottom:0cm;margin-left:18.0pt;mso-add-space:auto;
  text-align:left;text-indent:-18.0pt;line-height:normal;mso-list:l1 level1 lfo15"><!--[if !supportLists]--><span style="font-size:9.0pt;font-family:Symbol;mso-fareast-font-family:Symbol;
  mso-bidi-font-family:Symbol;color:black"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span></span><!--[endif]--><span style="font-size:9.0pt;mso-bidi-font-family:Arial;color:#0070C0">Y</span><span style="font-size:9.0pt;mso-bidi-font-family:Arial;color:black"> (YES) </span><span style="font-size:9.0pt;font-family:Wingdings;mso-fareast-font-family:Wingdings;
  mso-bidi-font-family:Wingdings;color:black">à</span><span style="font-size:
  9.0pt;mso-bidi-font-family:Arial;color:black"> INVISIBLE_ REP_LEGAUX actif<o:p></o:p></span></p>
  <p class="MsoListParagraphCxSpLast" align="left" style="margin-top:0cm;
  margin-right:0cm;margin-bottom:0cm;margin-left:18.0pt;mso-add-space:auto;
  text-align:left;text-indent:-18.0pt;line-height:normal;mso-list:l1 level1 lfo15"><!--[if !supportLists]--><span style="font-size:9.0pt;font-family:Symbol;mso-fareast-font-family:Symbol;
  mso-bidi-font-family:Symbol;color:black"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span></span><!--[endif]--><span style="font-size:9.0pt;mso-bidi-font-family:Arial;color:#0070C0">N</span><span style="font-size:9.0pt;mso-bidi-font-family:Arial;color:black"> (No) </span><span style="font-size:9.0pt;font-family:Wingdings;mso-fareast-font-family:Wingdings;
  mso-bidi-font-family:Wingdings;color:black">à</span><span style="font-size:
  9.0pt;mso-bidi-font-family:Arial;color:black"> INVISIBLE_ REP_LEGAUX non
  actif<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-5.3<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Name Of Coding System<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span class="SpellE"><span class="GramE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0">expandedYes</span></span><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0">-NoIndicator</span></span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;mso-yfti-lastrow:yes">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-11<o:p></o:p></span></p>
  </td>
  <td width="170" valign="top" style="width:127.65pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Observation <span class="SpellE">Result</span>
  Status<o:p></o:p></span></p>
  </td>
  <td width="302" valign="top" style="width:8.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Valeur fixée à «&nbsp;</span><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0">F&nbsp;</span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">»&nbsp;<o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

###### Modification Confidentiality Code
Cet OBX permet d’informer le Consommateur que la transaction porte une modification du CONFIDENTIALITY CODE indiquant une mise à jour de la métadonnée de mise en visibilité du document au patients et/ou aux représentants légaux.
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="652" style="width:488.8pt;border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes">
  <td width="652" colspan="3" valign="top" style="width:488.8pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Composition du groupe OBSERVATION/OBXNTE&nbsp;: Usage&nbsp;= <span class="SpellE">Required</span> / Cardinalité&nbsp;= [<span class="GramE">1..</span>1]<o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  background:#D9D9D9;mso-background-themecolor:background1;mso-background-themeshade:
  217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Elément requis&nbsp;:<o:p></o:p></span></b></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Description&nbsp;: <o:p></o:p></span></b></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Valeur&nbsp;: <o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Segment OBX<o:p></o:p></span></b></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">Observation/<span class="SpellE">Result</span><o:p></o:p></span></b></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-1<o:p></o:p></span></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Set Id - <span class="SpellE">Obx</span><o:p></o:p></span></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;mso-bidi-font-weight:bold">Numéro
  de séquence du segment<o:p></o:p></span></p>
  <p class="MsoNormal" style="margin-bottom:0cm"><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0;mso-bidi-font-weight:
  bold">6<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-2<o:p></o:p></span></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Value Type<o:p></o:p></span></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0;mso-bidi-font-weight:bold">CWE </span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black;mso-bidi-font-weight:bold">(<span class="SpellE">Coded</span> <span class="SpellE">with</span> Exceptions)</span><b style="mso-bidi-font-weight:
  normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-3<o:p></o:p></span></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Observation Identifier <o:p></o:p></span></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><b style="mso-bidi-font-weight:normal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p>&nbsp;</o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.1&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Code&nbsp;: <o:p></o:p></span></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0">MODIF_CONF_CODE<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.2&nbsp;:<span style="mso-spacerun:yes">&nbsp; </span><o:p></o:p></span></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Libellé&nbsp;:<o:p></o:p></span></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:#0070C0">Modification <span class="SpellE">Confidentiality</span>
  Code<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-3.3&nbsp;:<o:p></o:p></span></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Name of Coding system<o:p></o:p></span></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span class="SpellE"><span style="font-size:9.0pt;
  line-height:115%;color:#0070C0">MetaDMPMSS</span></span><span style="font-size:9.0pt;line-height:115%;color:#4472C4;mso-themecolor:accent5"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-5<o:p></o:p></span></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Observation Value<o:p></o:p></span></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">&gt; OBX-5.1<o:p></o:p></span></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Code&nbsp;: <o:p></o:p></span></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Table HL7 : 0136&nbsp;:</span><span style="font-size:8.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></p>
  <p class="MsoListParagraphCxSpFirst" style="margin-bottom:0cm;mso-add-space:
  auto;text-indent:-18.0pt;line-height:normal;mso-list:l32 level1 lfo30"><!--[if !supportLists]--><span style="font-size:9.0pt;mso-fareast-font-family:Arial;mso-bidi-font-family:
  Arial;color:black"><span style="mso-list:Ignore">-<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  </span></span></span><!--[endif]--><span style="font-size:9.0pt;mso-bidi-font-family:
  Arial;color:#0070C0">Y</span><span style="font-size:9.0pt;mso-bidi-font-family:
  Arial;color:black"> (Yes) </span><span style="font-size:9.0pt;font-family:
  Wingdings;mso-fareast-font-family:Wingdings;mso-bidi-font-family:Wingdings;
  color:black">à</span><span style="font-size:9.0pt;mso-bidi-font-family:Arial;
  color:black"> MODIF_CONF_CODE actif<u><o:p></o:p></u></span></p>
  <p class="MsoListParagraphCxSpLast" style="margin-bottom:0cm;mso-add-space:
  auto;text-indent:-18.0pt;line-height:normal;mso-list:l32 level1 lfo30"><!--[if !supportLists]--><span style="mso-fareast-font-family:Arial;mso-bidi-font-family:Arial;color:black"><span style="mso-list:Ignore">-<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  </span></span></span><!--[endif]--><span style="font-size:9.0pt;mso-bidi-font-family:
  Arial;color:#0070C0">N</span><span style="font-size:9.0pt;mso-bidi-font-family:
  Arial;color:black"> (No) </span><span style="font-size:9.0pt;font-family:
  Wingdings;mso-fareast-font-family:Wingdings;mso-bidi-font-family:Wingdings;
  color:black">à</span><span style="font-size:9.0pt;mso-bidi-font-family:Arial;
  color:black"> MODIF_CONF_CODE non Actif</span><u><span style="mso-bidi-font-family:
  Arial;color:black"><o:p></o:p></span></u></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">&gt; OBX-5.3</span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Name Of Coding System</span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span class="SpellE"><span class="GramE"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:#0070C0">expandedYes</span></span><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0">-NoIndicator</span></span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12;mso-yfti-lastrow:yes">
  <td width="179" valign="top" style="width:134.35pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">OBX-11</span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black"><o:p></o:p></span></p>
  </td>
  <td width="179" valign="top" style="width:134.35pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black;mso-bidi-font-weight:bold">Observation <span class="SpellE">Result</span>
  Status</span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black"><o:p></o:p></span></p>
  </td>
  <td width="293" valign="top" style="width:220.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:
  Arial;color:black">Valeur fixée à «&nbsp;</span><span style="font-size:9.0pt;
  line-height:115%;mso-bidi-font-family:Arial;color:#0070C0">F&nbsp;</span><span style="font-size:9.0pt;line-height:115%;mso-bidi-font-family:Arial;
  color:black">»&nbsp;<o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>
Un exemple est disponible [ici](exemples.html).

### Le message d’acquittement HL7v2

#### Profil du message ACK
Le profil du message ACK est le suivant :
<table>
<thead>
<tr>
<td style="background-color: grey; width: 132px;" width="132">
<p>Segment</p>
</td>
<td style="background-color: grey; width: 132px;" width="312">
<p>Meaning</p>
</td>
<td style="background-color: grey; width: 132px;" width="57">
<p>Usage</p>
</td>
<td style="background-color: grey; width: 132px;" width="47">
<p>Card.</p>
</td>
<td style="background-color: grey; width: 132px;" width="57">
<p>HL7 &sect;</p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td width="132">
<p>MSH</p>
</td>
<td width="312">
<p>Message header</p>
</td>
<td width="57">
<p>R</p>
</td>
<td width="47">
<p>[1..1]</p>
</td>
<td width="57">
<p>2</p>
</td>
</tr>
<tr>
<td width="132">
<p>[{SFT}]</p>
</td>
<td width="312">
<p>Software segment</p>
</td>
<td width="57">
<p>O</p>
</td>
<td width="47">
<p>[0..*]</p>
</td>
<td width="57">
<p>2</p>
</td>
</tr>
<tr>
<td width="132">
<p>[UAC]</p>
</td>
<td width="312">
<p>User Authentication Credential</p>
</td>
<td width="57">
<p>O</p>
</td>
<td width="47">
<p>[0..1]</p>
</td>
<td width="57">
<p>2</p>
</td>
</tr>
<tr>
<td width="132">
<p>MSA</p>
</td>
<td width="312">
<p>Message Acknowledgement</p>
</td>
<td width="57">
<p>R</p>
</td>
<td width="47">
<p>[1..1]</p>
</td>
<td width="57">
<p>2</p>
</td>
</tr>
<tr>
<td width="132">
<p>[{ERR}]</p>
</td>
<td width="312">
<p>Error</p>
</td>
<td width="57">
<p>C</p>
</td>
<td width="47">
<p>[0..*]</p>
</td>
<td width="57">
<p>2</p>
</td>
</tr>
</tbody>
</table>

#### Structure fonctionnelle du message
Après réception du message MDM, le LPS (DPI ou RIS dans le contexte SEGUR vague 2) va acquitter le message. Ci-dessous la structure du message ACK :
<div class="figure" style='text-align: center;'>
    <img src="image21.png" alt="Figure 15" title="Figure 15 : Description fonctionnelle du message ACK
" style="width:80%;">
    <figcaption><b>Figure 15 : Description fonctionnelle du message ACK</b></figcaption>
</div>    
<br>
Ces segments doivent être conformes au standard HL7v2.6.

#### Description des contraintes à appliquer sur le message ACK
##### Segment MSH
Le segment MSH reprend une partie des informations du message initial :
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="652" style="width:488.8pt;border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes">
  <td width="326" colspan="2" valign="top" style="width:244.4pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="center" style="text-align:center"><b><span style="color:black">Message initial<o:p></o:p></span></b></p>
  </td>
  <td width="326" colspan="2" valign="top" style="width:244.4pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="center" style="text-align:center"><b><span style="color:black">Message d’acquittement<o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="163" valign="top" style="width:122.2pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  background:#D9D9D9;mso-background-themecolor:background1;mso-background-themeshade:
  217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="center" style="text-align:center"><b><span style="color:black">Champ<o:p></o:p></span></b></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="center" style="text-align:center"><b><span style="color:black">Description</span><o:p></o:p></b></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="center" style="text-align:center"><b><span style="color:black">Champ</span><o:p></o:p></b></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="center" style="text-align:center"><b><span style="color:black">Description<o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="163" valign="top" style="width:122.2pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.3" target="_blank"><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:#0563C1;position:relative;top:.5pt;
  mso-text-raise:-.5pt;mso-fareast-language:FR">MSH.3</span></a></span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Arial;
  color:black;position:relative;top:.5pt;mso-text-raise:-.5pt;mso-fareast-language:
  FR"><span style="mso-spacerun:yes">&nbsp;</span>- <span class="SpellE">Sending</span>
  Application</span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black;mso-fareast-language:FR">&ZeroWidthSpace;</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Application source du message à
  acquitter <o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.5" target="_blank"><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:#0563C1;position:relative;top:.5pt;
  mso-text-raise:-.5pt;mso-fareast-language:FR">MSH.5</span></a></span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Arial;
  color:black;position:relative;top:.5pt;mso-text-raise:-.5pt;mso-fareast-language:
  FR"><span style="mso-spacerun:yes">&nbsp;</span>- <span class="SpellE">Receiving</span>
  Application</span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black;mso-fareast-language:FR">&ZeroWidthSpace;</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Application destinatrice de
  l’acquittement<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="163" valign="top" style="width:122.2pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.4" target="_blank"><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:#0563C1;position:relative;top:.5pt;
  mso-text-raise:-.5pt;mso-fareast-language:FR">MSH.4</span></a></span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Arial;
  color:black;position:relative;top:.5pt;mso-text-raise:-.5pt;mso-fareast-language:
  FR"><span style="mso-spacerun:yes">&nbsp;</span>- <span class="SpellE">Sending</span>
  Facility</span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black;mso-fareast-language:FR">&ZeroWidthSpace;</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Facility source du message à
  acquitter<o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6" target="_blank"><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:#0563C1;position:relative;top:.5pt;
  mso-text-raise:-.5pt;mso-fareast-language:FR">MSH.6</span></a></span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Arial;
  color:black;position:relative;top:.5pt;mso-text-raise:-.5pt;mso-fareast-language:
  FR"><span style="mso-spacerun:yes">&nbsp;</span>- <span class="SpellE">Receiving</span>
  Facility</span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black;mso-fareast-language:FR">&ZeroWidthSpace;</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Etablissement destinataire de
  l’acquittement<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4">
  <td width="163" valign="top" style="width:122.2pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.5" target="_blank"><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:#0563C1;position:relative;top:.5pt;
  mso-text-raise:-.5pt;mso-fareast-language:FR">MSH.5</span></a></span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Arial;
  color:black;position:relative;top:.5pt;mso-text-raise:-.5pt;mso-fareast-language:
  FR"><span style="mso-spacerun:yes">&nbsp;</span>- <span class="SpellE">Receiving</span>
  Application</span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black;mso-fareast-language:FR">&ZeroWidthSpace;</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Application destinatrice du
  message à acquitter<o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.3" target="_blank"><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:#0563C1;position:relative;top:.5pt;
  mso-text-raise:-.5pt;mso-fareast-language:FR">MSH.3</span></a></span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Arial;
  color:black;position:relative;top:.5pt;mso-text-raise:-.5pt;mso-fareast-language:
  FR"><span style="mso-spacerun:yes">&nbsp;</span>- <span class="SpellE">Sending</span>
  Application</span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black;mso-fareast-language:FR">&ZeroWidthSpace;</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Application source de
  l’acquittement<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5">
  <td width="163" valign="top" style="width:122.2pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6" target="_blank"><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:#0563C1;position:relative;top:.5pt;
  mso-text-raise:-.5pt;mso-fareast-language:FR">MSH.6</span></a></span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Arial;
  color:black;position:relative;top:.5pt;mso-text-raise:-.5pt;mso-fareast-language:
  FR"><span style="mso-spacerun:yes">&nbsp;</span>- <span class="SpellE">Receiving</span>
  Facility</span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black;mso-fareast-language:FR">&ZeroWidthSpace;</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Facility destinatrice du message
  à acquitter<o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.4" target="_blank"><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:#0563C1;position:relative;top:.5pt;
  mso-text-raise:-.5pt;mso-fareast-language:FR">MSH.4</span></a></span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Arial;
  color:black;position:relative;top:.5pt;mso-text-raise:-.5pt;mso-fareast-language:
  FR"><span style="mso-spacerun:yes">&nbsp;</span>- <span class="SpellE">Sending</span>
  Facility</span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black;mso-fareast-language:FR">&ZeroWidthSpace;</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Etablissement source de
  l’acquittement<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6;mso-yfti-lastrow:yes">
  <td width="163" valign="top" style="width:122.2pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.11" target="_blank"><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:#0563C1;position:relative;top:.5pt;
  mso-text-raise:-.5pt;mso-fareast-language:FR">MSH.11</span></a></span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Arial;
  color:black;position:relative;top:.5pt;mso-text-raise:-.5pt;mso-fareast-language:
  FR"><span style="mso-spacerun:yes">&nbsp;</span>- <span class="SpellE">Processing</span>
  Id</span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:
  Arial;color:black;mso-fareast-language:FR">&ZeroWidthSpace;</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Identifiant de traitement <o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.11" target="_blank"><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:#0563C1;position:relative;top:.5pt;
  mso-text-raise:-.5pt;mso-fareast-language:FR">MSH.11</span></a></span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:Arial;
  color:black;position:relative;top:.5pt;mso-text-raise:-.5pt;mso-fareast-language:
  FR"><span style="mso-spacerun:yes">&nbsp;</span>- <span class="SpellE">Processing</span>
  Id</span><span style="mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:
  Arial;color:black;mso-fareast-language:FR">&ZeroWidthSpace;</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="163" valign="top" style="width:122.2pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Identifiant de traitement<o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

Le champ MSH.9 « Message type » prend la valeur : `ACK^T02^ACK` ou `ACK^T04^ACK` ou `ACK^T10^ACK` selon l’évènement du message initial.

<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" style="border-collapse:collapse;mso-table-layout-alt:fixed;border:none;
 mso-border-alt:solid windowtext .5pt;mso-yfti-tbllook:1184;mso-padding-alt:
 0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:46.5pt">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;
  height:46.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="color:black">Champ<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:46.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="color:black">Contenu<o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:46.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="color:black">Type donnée<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:46.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="color:black">Caractère optionnel/obligatoire<o:p></o:p></span></p>
  <p class="MsoNormal"><span style="color:black"><o:p>&nbsp;</o:p></span></p>
  <p class="MsoNormal"><span style="color:black"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-1<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:#4472C4;mso-themecolor:accent5">|</span><span style="color:black"> séparateur de champ<o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">ST<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-2<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:#4472C4;mso-themecolor:accent5">^~\&amp;</span><span style="color:black">&nbsp;: séparateur de composant, répétition, caractère
  d’échappement, séparateur de sous-composants<o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">ST<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-3<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Application émettrice<o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">HD<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-4<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Organisation émettrice<o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">HD<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:5">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-5<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Application réceptrice<o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">HD<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:6">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-6<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Organisation réceptrice<o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">HD<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:7">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-7<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Date/time du message<o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">TS<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:8">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-9<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Type du message, selon
  l’évènement du message initial&nbsp;:</span><span style="color:#0070C0"><o:p></o:p></span></p>
  <p class="MsoNormal"><span lang="EN-US" style="color:#0070C0;mso-ansi-language:
  EN-US">ACK^T02^ACK ACK^T04^ACK ACK^T10^ACK.<o:p></o:p></span></p>
  <p class="MsoNormal"><span lang="EN-US" style="color:black;mso-ansi-language:
  EN-US"><o:p>&nbsp;</o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSG<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  <p class="MsoNormal"><span style="color:black"><o:p>&nbsp;</o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:9">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-10<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Identifiant du message<o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">ST<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:10">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-11<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span class="SpellE"><span style="color:black">Processing</span></span><span style="color:black"> Id<br>
  </span><span style="color:#0070C0">P&nbsp;</span>: en production<span style="color:#4472C4;mso-themecolor:accent5"><br>
  </span><span style="color:#0070C0">T&nbsp;</span>: message de test<span style="color:#4472C4;mso-themecolor:accent5"><br>
  </span><span style="color:#0070C0">D&nbsp;</span>: environnement de <span class="SpellE">debug</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">PT<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:11">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-12<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Version du standard</span><span style="color:#4472C4;mso-themecolor:accent5"><br>
  </span><span style="color:#0070C0">2.6 </span>pour MDM<span style="color:
  #4472C4;mso-themecolor:accent5"><o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">VID<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:12">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-17<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:#0070C0">FRA</span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">ID<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:13;mso-yfti-lastrow:yes">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">MSH-18<o:p></o:p></span></p>
  </td>
  <td width="196" valign="top" style="width:147.15pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">Jeux de caractères, valeurs
  possibles&nbsp;:<o:p></o:p></span></p>
  <p class="MsoNormal"><span style="color:#0070C0">UNICODE UTF-8 </span>ou <span style="color:#0070C0">8859/15 </span><span style="color:#4472C4;mso-themecolor:
  accent5"><br style="mso-special-character:line-break">
  <!--[if !supportLineBreakNewLine]--><br style="mso-special-character:line-break">
  <!--[endif]--></span><span style="color:black"><o:p></o:p></span></p>
  </td>
  <td width="87" valign="top" style="width:65.45pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">ID<o:p></o:p></span></p>
  </td>
  <td width="161" valign="top" style="width:120.5pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

##### Segment MSA
Le segment MSA contient à minima les champs suivants : 
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" style="border-collapse:collapse;border:none;mso-border-alt:solid windowtext .5pt;
 mso-yfti-tbllook:1184;mso-padding-alt:0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes">
  <td width="189" valign="top" style="width:141.5pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="center" style="text-align:center"><b><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;line-height:115%;color:black">Champ
  requis</span></b><b><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;
  line-height:115%"><o:p></o:p></span></b></p>
  </td>
  <td width="461" valign="top" style="width:345.6pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal" align="center" style="text-align:center"><b><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;line-height:115%;color:black">Contenu</span></b><b><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;line-height:115%"><o:p></o:p></span></b></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="189" valign="top" style="width:141.5pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;line-height:115%">MSA.1</span></a></span><span class="cx-body"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;
  line-height:115%;color:black"> - <span class="SpellE">Acknowledgment</span>
  Code</span></span><b><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;
  line-height:115%;color:black"><o:p></o:p></span></b></p>
  </td>
  <td width="461" valign="top" style="width:345.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;
  line-height:115%;mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:
  Arial;color:black;mso-fareast-language:FR">Code d’acquittement du
  message&nbsp;: <o:p></o:p></span></p>
  <p class="MsoListParagraphCxSpFirst" style="margin-top:0cm;margin-right:0cm;
  margin-bottom:0cm;margin-left:18.0pt;mso-add-space:auto;text-indent:-18.0pt;
  line-height:normal;mso-list:l1 level1 lfo15"><!--[if !supportLists]--><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:Symbol;
  mso-fareast-font-family:Symbol;mso-bidi-font-family:Symbol;color:black"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  </span></span></span><!--[endif]--><span style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt;mso-fareast-font-family:Calibri;mso-fareast-theme-font:minor-latin;
  mso-bidi-font-family:Arial;color:black">AA (</span><span style="font-size:
  9.0pt;mso-bidi-font-size:10.0pt;mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black;mso-fareast-language:FR">Original <span class="GramE">mode:</span> Application <span class="SpellE">Accept</span> – (<span class="SpellE">Enhanced</span> mode: Application <span class="SpellE">acknowledgment</span>:
  <span class="SpellE">Accept</span>) </span><span style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt;mso-fareast-font-family:Calibri;mso-fareast-theme-font:
  minor-latin;mso-bidi-font-family:Arial;color:black">: le message a été
  compris et intégré par&nbsp;l’application</span><span style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt;mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black;mso-fareast-language:FR"> destinatrice
  qui prend la responsabilité du message et libère ainsi l’application
  productrice de toute obligation de le renvoyer.</span><span style="font-size:
  9.0pt;mso-bidi-font-size:10.0pt;mso-fareast-font-family:Calibri;mso-fareast-theme-font:
  minor-latin;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></p>
  <p class="MsoListParagraphCxSpMiddle" style="margin-top:0cm;margin-right:0cm;
  margin-bottom:0cm;margin-left:18.0pt;mso-add-space:auto;text-indent:-18.0pt;
  line-height:normal;mso-list:l1 level1 lfo15"><!--[if !supportLists]--><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:Symbol;
  mso-fareast-font-family:Symbol;mso-bidi-font-family:Symbol;color:black"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  </span></span></span><!--[endif]--><span style="font-size:9.0pt;mso-bidi-font-size:
  10.0pt;mso-fareast-font-family:Calibri;mso-fareast-theme-font:minor-latin;
  mso-bidi-font-family:Arial;color:black">AE </span><span style="font-size:
  9.0pt;mso-bidi-font-size:10.0pt;mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black;mso-fareast-language:FR">(Original <span class="GramE">mode:</span> Application <span class="SpellE">Error</span> - <span class="SpellE">Enhanced</span> mode: Application <span class="SpellE">acknowledgment</span>:
  <span class="SpellE">Error</span>) </span><span style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt;mso-fareast-font-family:Calibri;mso-fareast-theme-font:
  minor-latin;mso-bidi-font-family:Arial;color:black">: le message contient des
  erreurs de syntaxe.&nbsp;&nbsp;</span><span style="font-size:9.0pt;
  mso-bidi-font-size:10.0pt;mso-fareast-font-family:&quot;Times New Roman&quot;;
  mso-bidi-font-family:Arial;color:black">&nbsp;</span><span style="font-size:
  9.0pt;mso-bidi-font-size:10.0pt;mso-fareast-font-family:Calibri;mso-fareast-theme-font:
  minor-latin;mso-bidi-font-family:Arial;color:black"><o:p></o:p></span></p>
  <p class="MsoListParagraphCxSpLast" style="margin-top:0cm;margin-right:0cm;
  margin-bottom:0cm;margin-left:18.0pt;mso-add-space:auto;text-indent:-18.0pt;
  line-height:normal;mso-list:l1 level1 lfo15"><!--[if !supportLists]--><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;font-family:Symbol;
  mso-fareast-font-family:Symbol;mso-bidi-font-family:Symbol;color:black;
  mso-fareast-language:FR"><span style="mso-list:Ignore">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span></span><!--[endif]--><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;mso-fareast-font-family:
  &quot;Times New Roman&quot;;mso-bidi-font-family:Arial;color:black;mso-fareast-language:
  FR">AR (Original <span class="GramE">mode:</span> Application <span class="SpellE">Reject</span> - <span class="SpellE">Enhanced</span> mode:
  Application <span class="SpellE">acknowledgment</span>: <span class="SpellE">Reject</span>)
   : le message est rejeté pour une raison circonstancielle. Il peut être
  réémis plus tard.&nbsp;<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2;mso-yfti-lastrow:yes">
  <td width="189" valign="top" style="width:141.5pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black"><a href="https://hl7-definition.caristix.com/v2/HL7v2.8/Fields/MSH.6"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;line-height:115%">MSA.2</span></a></span><span class="cx-body"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;
  line-height:115%;color:black"> - Message Control Id</span></span><b><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;line-height:115%;color:black"><o:p></o:p></span></b></p>
  </td>
  <td width="461" valign="top" style="width:345.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;
  line-height:115%;mso-fareast-font-family:&quot;Times New Roman&quot;;mso-bidi-font-family:
  Arial;color:black;mso-fareast-language:FR">Rappel l’identifiant du message
  acquitté correspondant au champ MSH.10 du message initial.</span><span style="font-size:9.0pt;mso-bidi-font-size:10.0pt;line-height:115%;color:black">
  <o:p></o:p></span></p>
  </td>
 </tr>
</tbody></table>

##### Segment ERR
Ce segment est utilisé au niveau des messages d’acquittement HL7 dans le cas où le champ MSA-1 prend la valeur AE (Application error).

Le tableau ci-dessous liste les champs à renseigner pour le segment ERR :
<table class="MsoTableGrid" border="1" cellspacing="0" cellpadding="0" width="699" style="border-collapse:collapse;mso-table-layout-alt:fixed;border:none;
 mso-border-alt:solid windowtext .5pt;mso-yfti-tbllook:1184;mso-padding-alt:
 0cm 5.4pt 0cm 5.4pt">
 <tbody><tr style="mso-yfti-irow:0;mso-yfti-firstrow:yes;height:23.5pt">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  mso-border-alt:solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:
  background1;mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;
  height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="color:black">Champ<o:p></o:p></span></p>
  </td>
  <td width="283" valign="top" style="width:212.6pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="color:black">Contenu<o:p></o:p></span></p>
  </td>
  <td width="76" valign="top" style="width:2.0cm;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="color:black">Type donnée<o:p></o:p></span></p>
  </td>
  <td width="246" valign="top" style="width:184.3pt;border:solid windowtext 1.0pt;
  border-left:none;mso-border-left-alt:solid windowtext .5pt;mso-border-alt:
  solid windowtext .5pt;background:#D9D9D9;mso-background-themecolor:background1;
  mso-background-themeshade:217;padding:0cm 5.4pt 0cm 5.4pt;height:23.5pt">
  <p class="MsoNormal" align="center" style="text-align:center"><span style="color:black">Caractère optionnel/obligatoire<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:1">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">ERR-2<o:p></o:p></span></p>
  </td>
  <td width="283" valign="top" style="width:212.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="mso-bidi-font-family:Arial;color:black">Localisation
  de l’erreur dans le cas d’une erreur de syntaxe du message initial.<o:p></o:p></span></p>
  </td>
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">ERL<o:p></o:p></span></p>
  </td>
  <td width="246" valign="top" style="width:184.3pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">O<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:2">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">ERR-3<o:p></o:p></span></p>
  </td>
  <td width="283" valign="top" style="width:212.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal">Code erreur HL7 dont les valeurs sont à prendre dans la table
  HL7 0357 (nom symbolique&nbsp;: <span class="SpellE">messageErrorCondition</span>)<sup>
  <o:p></o:p></sup></p>
  </td>
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">CWE<o:p></o:p></span></p>
  </td>
  <td width="246" valign="top" style="width:184.3pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span class="GramE"><span style="color:black">R<sup>(</sup></span></span><sup><span style="color:black">Note 1) (Note 2)<o:p></o:p></span></sup></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:3">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">ERR-4<o:p></o:p></span></p>
  </td>
  <td width="283" valign="top" style="width:212.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal">Sévérité de l’erreur dont les valeurs sont à prendre dans
  la table HL7 0516 (nom symbolique&nbsp;: <span class="SpellE">errorSeverity</span>)</p>
  </td>
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">ID<o:p></o:p></span></p>
  </td>
  <td width="246" valign="top" style="width:184.3pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">R<o:p></o:p></span></p>
  </td>
 </tr>
 <tr style="mso-yfti-irow:4;mso-yfti-lastrow:yes">
  <td width="94" valign="top" style="width:70.65pt;border:solid windowtext 1.0pt;
  border-top:none;mso-border-top-alt:solid windowtext .5pt;mso-border-alt:solid windowtext .5pt;
  padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">ERR-5<o:p></o:p></span></p>
  </td>
  <td width="283" valign="top" style="width:212.6pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal">Code erreur du traitement applicatif du message HL7 dont
  les valeurs sont à prendre dans la table user-<span class="SpellE">defined</span>
  0533 (nom symbolique&nbsp;: <span class="SpellE">applicationErrorCode</span>)<sup><o:p></o:p></sup></p>
  </td>
  <td width="76" valign="top" style="width:2.0cm;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span style="color:black">CWE<o:p></o:p></span></p>
  </td>
  <td width="246" valign="top" style="width:184.3pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  mso-border-top-alt:solid windowtext .5pt;mso-border-left-alt:solid windowtext .5pt;
  mso-border-alt:solid windowtext .5pt;padding:0cm 5.4pt 0cm 5.4pt">
  <p class="MsoNormal"><span class="GramE"><span style="color:black">C<sup>(</sup></span></span><sup><span style="color:black">Note 1) (Note 2)<o:p></o:p></span></sup></p>
  </td>
 </tr>
</tbody></table>
_**(Note 1) :** les valeurs possibles pour les champs ERR-3 et ERR-5 sont listées dans les tables messageErrorCondition et applicationErrorCondition précisées [ici](error-codes.html)._

_**Note (2) :** dans le cas où le rejet du message HL7 MDM est dû à un problème applicatif au niveau du CONSOMMATEUR, le champ ERR-3 sera renseigné avec la valeur « 207 » (Application error) et le champ ERR-5 sera renseigné avec une valeur comprise dans la table applicationErrorCode. Dans le cas où le message MDM est rejeté par le système CONSOMMATEUR pour une raison technique, le champ ERR-3 sera renseigné avec une valeur comprise dans la table messageErrorCondition et le champ ERR-5 ne sera pas renseigné._

##### Exemple

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