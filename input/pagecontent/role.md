<table width="638">
<tbody>
<tr>
<td width="92">
<p><strong>Acteur :</strong></p>
</td>
<td width="547">
<p>GESTIONNAIRE</p>
</td>
</tr>
<tr>
<td width="92">
<p><strong>R&ocirc;le :</strong></p>
</td>
<td width="547">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le GESTIONNAIRE extrait les informations de l&rsquo;archive IHE_XDM (pi&egrave;ce jointe du mail), analyse ces informations et construit le message HL7 MDM correspondant pour l&rsquo;envoyer au CONSOMMATEUR.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le GESTIONNAIRE r&eacute;ceptionne l&rsquo;accus&eacute; de r&eacute;ception et d&rsquo;int&eacute;gration du message HL7 MDM, g&egrave;re cet accus&eacute; et construit un accus&eacute; de lecture MSSant&eacute; (MDN-Message Disposition Notification) en fonction du statut retourn&eacute; par l&rsquo;acquittement du message HL7 MDM.</p>
</td>
</tr>
<tr>
<td width="92">
<p><strong>Acteur :</strong></p>
</td>
<td width="547">
<p>CONSOMMATEUR</p>
</td>
</tr>
<tr>
<td width="92">
<p><strong>R&ocirc;le :</strong></p>
</td>
<td width="547">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le CONSOMMATEUR re&ccedil;oit la demande du GESTIONNAIRE (transmission initiale/remplacement/suppression d&rsquo;un document) sous la forme d&rsquo;un message HL7 MDM, int&egrave;gre si possible dans sa base de donn&eacute;es les informations port&eacute;es par le message HL7 MDM et renvoie vers le GESTIONNAIRE l&rsquo;accus&eacute; de r&eacute;ception du message HL7 MDM.</p>
</td>
</tr>
</tbody>
</table>