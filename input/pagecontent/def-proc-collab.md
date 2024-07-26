### Processus collaboratif « Demande de transmission initiale de document(s) »

<div class="figure" style='text-align: center;'>
    <img src="image15.png" alt="Figure 9" title="Figure 9 : Processus collaboratif « Demande de transmission initiale de document(s) » pour intégration au niveau du CONSOMMATEUR " style="width:60%;">
    <figcaption><b>Figure 9 : Processus collaboratif « Demande de transmission initiale de document(s) » pour intégration au niveau du CONSOMMATEUR</b></figcaption>
</div>    
<br>

<table>
<tbody>
<tr>
<td width="226">
<p><strong>Service Attendu</strong></p>
</td>
<td width="423">
<p>Le GESTIONNAIRE transmet au CONSOMMATEUR la demande d&rsquo;int&eacute;gration de(s) document(s) de sant&eacute; d'un patient re&ccedil;ue sur la BAL MSSant&eacute; destinatrice.</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Pr&eacute;-Conditions</strong></p>
</td>
<td width="423">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le patient est connu du CONSOMMATEUR.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le GESTIONNAIRE d&eacute;tecte qu'un courriel a &eacute;t&eacute; re&ccedil;u sur la BAL avec en pi&egrave;ce jointe une archive XDM.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le GESTIONNAIRE d&eacute;zippe l&rsquo;archive XDM. Il v&eacute;rifie qu&rsquo;elle contient des documents de sant&eacute; d&rsquo;un patient au format CDA ainsi qu&rsquo;un fichier de m&eacute;tadonn&eacute;es.</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Post-Conditions</strong></p>
</td>
<td width="423">
<p>Le GESTIONNAIRE trace les transmissions de document(s)</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Contraintes fonctionnelles</strong></p>
</td>
<td width="423">
<p>La BAL du GESTIONNAIRE doit &ecirc;tre en capacit&eacute; de d&eacute;tecter les courriels entrants avec demande de traitement sur le(s) document(s)</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Sc&eacute;nario Nominal</strong></p>
</td>
<td width="423">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Suite &agrave; la r&eacute;ception d&rsquo;un courriel sur la BAL destinatrice, le GESTIONNAIRE transmet le document de sant&eacute; de la pi&egrave;ce jointe au CONSOMMATEUR.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le CONSOMMATEUR traite la demande d&rsquo;int&eacute;gration du document.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le CONSOMMATEUR retourne au GESTIONNAIRE un accusé de réception de la demande d'intégration du document.</p>
</td>
</tr>
</tbody>
</table>

### Processus collaboratif « Demande de remplacement de document(s) »

<div class="figure" style='text-align: center;'>
    <img src="image16.png" alt="Figure 10" title="Figure 10 : Processus collaboratif « Demande de remplacement de document(s) » au niveau du CONSOMMATEUR" style="width:60%;">
    <figcaption><b>Figure 10 : Processus collaboratif « Demande de remplacement de document(s) » au niveau du CONSOMMATEUR</b></figcaption>
</div>    
<br>
Le processus « Demande de remplacement de document(s) » permet également de gérer la mise à jour des métadonnées associées au(x) document(s).

Ainsi, dans le cas d’une demande de mise à jour des métadonnées de masquage/démasquage aux PS et de visibilité du document au patient, une nouvelle version de document est générée par l’initiateur du courriel. Cette nouvelle version vient remplacer la précédente au niveau du CONSOMMATEUR (application métier destinatrice).

<table>
<tbody>
<tr>
<td width="226">
<p><strong>Service Attendu</strong></p>
</td>
<td width="423">
<p>Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de remplacement de(s) document(s) de sant&eacute; d'un patient re&ccedil;ue sur la BAL MSSant&eacute; destinatrice.</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Pr&eacute;-Conditions</strong></p>
</td>
<td width="423">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le patient est connu du CONSOMMATEUR.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le document doit &ecirc;tre valid&eacute; et identifi&eacute; comme rempla&ccedil;ant un document pr&eacute;c&eacute;demment envoy&eacute; par MSSant&eacute;.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le CONSOMMATEUR dispose de la derni&egrave;re version du document original dans sa base de donn&eacute;es.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le GESTIONNAIRE d&eacute;tecte qu'un courriel a &eacute;t&eacute; re&ccedil;u sur la BAL avec en pi&egrave;ce jointe une archive IHE_XDM.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le GESTIONNAIRE d&eacute;zippe l&rsquo;archive XDM. Il v&eacute;rifie qu&rsquo;elle contient des documents de sant&eacute; d&rsquo;un patient au format CDA ainsi qu&rsquo;un fichier de m&eacute;tadonn&eacute;es et prend connaissance du traitement &agrave; effectuer sur le(s) document(s)</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Post-Conditions</strong></p>
</td>
<td width="423">
<p>Le GESTIONNAIRE trace les transmissions de document(s)</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Contraintes fonctionnelles</strong></p>
</td>
<td width="423">
<p>La BAL du GESTIONNAIRE doit &ecirc;tre en capacit&eacute; de d&eacute;tecter les courriels entrants avec demande de traitement sur le(s) document(s)</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Sc&eacute;nario Nominal</strong></p>
</td>
<td width="423">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Suite &agrave; la r&eacute;ception du courriel sur la BAL destinatrice, le GESTIONNAIRE transmet la demande de remplacement de documents de sant&eacute; de la pi&egrave;ce jointe au CONSOMMATEUR</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le CONSOMMATEUR traite la demande de remplacement du document.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le CONSOMMATEUR retourne au GESTIONNAIRE un accus&eacute; de r&eacute;ception de la demande de remplacement du document.</p>
<p>&nbsp;</p>
</td>
</tr>
</tbody>
</table>

### Processus collaboratif « Demande de suppression de document(s) »

<div class="figure" style='text-align: center;'>
    <img src="image17.png" alt="Figure 11" title="Figure 11 : Processus collaboratif « Demande de suppression de document(s) » au niveau du CONSOMMATEUR" style="width:60%;">
    <figcaption><b>Figure 11 : Processus collaboratif « Demande de suppression de document(s) » au niveau du CONSOMMATEUR</b></figcaption>
</div>    
<br>

<table>
<tbody>
<tr>
<td width="226">
<p><strong>Service Attendu</strong></p>
</td>
<td width="423">
<p>Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de suppression de(s) document(s) de sant&eacute; d'un patient re&ccedil;ue sur la BAL MSSant&eacute; destinatrice.</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Pr&eacute;-Conditions</strong></p>
</td>
<td width="423">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le patient est connu du consommateur.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le document doit &ecirc;tre valid&eacute; et doit correspondre &agrave; la derni&egrave;re version du document envoy&eacute; au CONSOMMATEUR.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le CONSOMMATEUR dispose de la derni&egrave;re version du document original dans sa base de donn&eacute;es.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le GESTIONNAIRE d&eacute;tecte qu'un courriel a &eacute;t&eacute; re&ccedil;u sur la BAL avec en pi&egrave;ce jointe une archive IHE_XDM.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le GESTIONNAIRE d&eacute;zippe l&rsquo;archive XDM. Il v&eacute;rifie qu&rsquo;elle contient des documents de sant&eacute; d&rsquo;un patient au format CDA ainsi qu&rsquo;un fichier de m&eacute;tadonn&eacute;es et prend connaissance du traitement &agrave; effectuer sur le document</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Post-Conditions</strong></p>
</td>
<td width="423">
<p>Le GESTIONNAIRE trace les transmissions de document(s)</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Contraintes fonctionnelles</strong></p>
</td>
<td width="423">
<p>La BAL du GESTIONNAIRE doit &ecirc;tre en capacit&eacute; de d&eacute;tecter les courriels entrants avec demande de traitement sur le(s) document(s)</p>
</td>
</tr>
<tr>
<td width="226">
<p><strong>Sc&eacute;nario Nominal</strong></p>
</td>
<td width="423">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Suite &agrave; la r&eacute;ception d&rsquo;un courriel sur la BAL destinatrice, le GESTIONNAIRE transmet la demande de suppression du document de sant&eacute; de la pi&egrave;ce jointe au CONSOMMATEUR</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le CONSOMMATEUR traite la demande de suppression du document.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Le CONSOMMATEUR retourne au GESTIONNAIRE un accusé de réception de suppression du document.</p>
</td>
</tr>
</tbody>
</table>