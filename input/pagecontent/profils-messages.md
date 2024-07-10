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
Les contraintes apportées par ce volet sur les données du message MDM sont décrites à la section 12.2 [LIEN].

#### Description fonctionnelle du message MDM


