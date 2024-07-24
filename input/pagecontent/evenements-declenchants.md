Après réception d’un courriel détecté dans une BAL applicative MSSanté, la PFI ouvre l’archive IHE_XDM contenant des documents médicaux et les transmets individuellement au LPS consommateur en utilisant un message HL7v2.6 de type MDM.

Ensuite, le LPS accuse réception de cette demande de traitement sur le document avec un message HL7v2.6 de type ACK. 
<table width="680">
<tbody>
<tr>
<td style="background-color: grey; width: 217px;" width="217">
<p><strong>Flux m&eacute;tiers</strong></p>
</td>
<td style="background-color: grey; width: 217px;" width="463">
<p><strong>Type de message HL7v2.6</strong></p>
</td>
</tr>
<tr>
<td rowspan="3" width="217">
<p>TransmissionDocuments</p>
</td>
<td width="463">
<p>Transmission initiale d&rsquo;un document&nbsp;: L&rsquo;&eacute;v&egrave;nement utilis&eacute; sera le T02&nbsp;&laquo;&nbsp;Original document notification&nbsp;&raquo;</p>
<p>-&gt;&nbsp; MDM^T02^MDM_T02</p>
<p>-&gt;&nbsp; OBX-11 = F (Final results; Can only be changed with a corrected result.) [HL7 Tables 0085]</p>
</td>
</tr>
<tr>
<td width="463">
<p>Suppression d&rsquo;un document : L&rsquo;&eacute;v&egrave;nement utilis&eacute; sera le T04&nbsp;&laquo;&nbsp;Document status change notification and content&nbsp;&raquo;</p>
<p>-&gt;&nbsp; MDM^T04^MDM_T02</p>
<p>-&gt;&nbsp; OBX-11 = D (Deletes the OBX record) [HL7 Tables 0085]</p>
</td>
</tr>
<tr>
<td width="463">
<p>Remplacement d&rsquo;un document&nbsp;: L&rsquo;&eacute;v&egrave;nement utilis&eacute; sera le T10&nbsp;&laquo;&nbsp;Document replacement notification and content&nbsp;&raquo;</p>
<p>-&gt;&nbsp; MDM^T10^MDM_T02</p>
<p>-&gt;&nbsp; OBX-11 = C (Record coming over is a correction and thus replaces a final result) [HL7 Tables 0085]</p>
</td>
</tr>
<tr>
<td width="217">
<p>ReponseTransmissionDocuments</p>
</td>
<td width="463">
<p>ACK : Acquittement du message HL7 MDM</p>
</td>
</tr>
</tbody>
</table>