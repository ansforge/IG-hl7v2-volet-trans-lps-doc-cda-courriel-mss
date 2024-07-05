Les cas d'usages liés à une demande de transmission initiale/remplacement/suppression de document(s) clinique(s) d'un patient sont gérés différemment entre l'ORU et le MDM :

<table width="652">
<tbody>
<tr>
<td width="218">
<p><strong>Flux m&eacute;tier</strong></p>
</td>
<td width="217">
<p><strong>Message de type ORU</strong></p>
</td>
<td width="217">
<p><strong>Message de type MDM</strong></p>
</td>
</tr>
<tr>
<td width="218">
<p>TransmissionDocuments&nbsp;: Demande de transmission initiale de document(s)</p>
</td>
<td width="217">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ORU : L&rsquo;&eacute;v&egrave;nement utilis&eacute; sera le R01 &laquo;&nbsp;Unsolicited Observation Message&nbsp;&raquo;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;-&gt; OBX-11 = F (Final results; Can only be changed with a corrected result.) [HL7 Tables 0085]</p>
</td>
<td width="217">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MDM&nbsp;: L&rsquo;&eacute;v&egrave;nement utilis&eacute; sera le T02&nbsp;&laquo;&nbsp;Original document notification&nbsp;&raquo;</p>
<p>&nbsp;</p>
<p>-&gt; MDM^T02^MDM_T02</p>
<p><strong><u>&nbsp;</u></strong></p>
<p>-&gt; OBX-11 = F (Final results; Can only be changed with a corrected result.) [HL7 Tables 0085]</p>
</td>
</tr>
<tr>
<td width="218">
<p>TransmissionDocuments&nbsp;: Demande de suppression de document(s)</p>
</td>
<td width="217">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ORU : L&rsquo;&eacute;v&egrave;nement utilis&eacute; sera le R01 &laquo;&nbsp;Unsolicited Observation Message&nbsp;&raquo;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>-&gt; OBX-11 = D (Deletes the OBX record) [HL7 Tables 0085]</p>
</td>
<td width="217">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MDM&nbsp;: L&rsquo;&eacute;v&egrave;nement utilis&eacute; sera le T04&nbsp;&laquo;&nbsp;Document status change notification and content&nbsp;&raquo;</p>
<p>&nbsp;</p>
<p>-&gt; MDM^T04^MDM_T02</p>
<p><strong><u>&nbsp;</u></strong></p>
<p>-&gt; OBX-11 = D (Deletes the OBX record) [HL7 Tables 0085]</p>
</td>
</tr>
<tr>
<td width="218">
<p>TransmissionDocuments&nbsp;: Demande de remplacement de document(s)</p>
</td>
<td width="217">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ORU : L&rsquo;&eacute;v&egrave;nement utilis&eacute; sera le R01 &laquo;&nbsp;Unsolicited Observation Message&nbsp;&raquo;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>-&gt; OBX-11 = C (Record coming over is a correction and thus replaces a final result) [HL7 Tables 0085]</p>
</td>
<td width="217">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MDM&nbsp;: L&rsquo;&eacute;v&egrave;nement utilis&eacute; sera le T10&nbsp;&laquo;&nbsp;Document replacement notification and content&nbsp;&raquo;</p>
<p><strong><u>&nbsp;</u></strong></p>
<p>-&gt; MDM^T10^MDM_T02<br /> </p>
<p>-&gt; OBX-11 = C (Record coming over is a correction and thus replaces a final result) [HL7 Tables 0085]</p>
</td>
</tr>
<tr>
<td width="218">
<p>R&eacute;ponseTransmissionDocuments&nbsp;</p>
</td>
<td width="217">
<p>Acquittement technique du message HL7 ORU</p>
</td>
<td width="217">
<p>Acquittement technique du message HL7 MDM</p>
</td>
</tr>
</tbody>
</table>