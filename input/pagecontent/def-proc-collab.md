Pour l'ensemble des processus décrits :

-   L'accusé de réception MSSanté correspond à la prise en compte du courriel par le serveur de messagerie du destinataire du courriel,

-   L'accusé de lecture MSSanté défini par la RFC 8098 (Message Disposition Notification) comprend un élément dénommé Disposition types qui rend compte à l'expéditeur du courriel du traitement advenu sur ce courriel au niveau du destinataire : lecture du courriel, transfert du courriel, traitement automatique du courriel, suppression du courriel.

### Processus collaboratif « Demande de transmission initiale de document(s) »

<div class="figure">
    <img src="image13.png" alt="Figure 9" title="Figure 9 : Processus collaboratif « Demande de transmission initiale de document(s) » pour publication sur DMP et envoi par MSS" style="width:100%;">
    <figcaption>Figure 9 : Processus collaboratif « Demande de transmission initiale de document(s) » pour publication sur DMP et envoi par MSS</figcaption>
</div>    
<br>

<table width="650">
<tbody>
<tr>
<td width="151">
<p><strong>Service Attendu</strong></p>
</td>
<td width="499">
<p>Le CREATEUR &eacute;met le(s) document(s) valid&eacute;(s) vers le GESTIONNAIRE qui publie ce(s) document(s) sur le DMP et/ou r&eacute;alise un envoi par MSSant&eacute;.</p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Pr&eacute;-Conditions</strong></p>
</td>
<td width="499">
<p>Les m&eacute;tadonn&eacute;es de contexte DMP/MSSant&eacute; doivent &ecirc;tre renseign&eacute;es (soit par param&eacute;trage de l&rsquo;application soit par l&rsquo;utilisateur) et l&rsquo;utilisateur doit valider ce(s) document(s) au niveau de l&rsquo;application m&eacute;tier dans laquelle il a &eacute;t&eacute; g&eacute;n&eacute;r&eacute; via un statut de validation g&eacute;r&eacute; en interne. Chaque document CDA doit &ecirc;tre valide et disponible.</p>
<p>L&rsquo;INS du patient est obligatoirement qualifi&eacute;e dans le cas o&ugrave; la publication sur le DMP est demand&eacute;e.</p>
<p>Une d&eacute;rogation valable jusqu&rsquo;&agrave; fin 2023, puis renouvelable jusqu&rsquo;&agrave; sa r&eacute;vocation qui sera indiqu&eacute;e dans les futures versions du r&eacute;f&eacute;rentiel socle MSSant&eacute;#2, permet d&rsquo;&eacute;changer un courriel par MSSant&eacute; en l&rsquo;absence d&rsquo;un INS qualifi&eacute;.</p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Post-Conditions</strong></p>
</td>
<td width="499">
<p>Le document est partag&eacute; sur le DMP et/ou re&ccedil;u par le(s) destinataire(s) via MSSant&eacute;.</p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Contraintes fonctionnelles</strong></p>
</td>
<td width="499">
<p>Dans le cas o&ugrave; le CREATEUR de documents transmet les 2 formats de documents s&eacute;par&eacute;ment (CDA Niv1 et CDA Niv3), ces 2 documents sont transmis simultan&eacute;ment dans la m&ecirc;me transaction. (<em>Note1)</em></p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Sc&eacute;nario Nominal</strong></p>
</td>
<td width="499">
<p>Le CREATEUR transmet une demande de transmission initiale de document(s) au GESTIONNAIRE en pr&eacute;cisant si ce(s) document(s) doit(vent) &ecirc;tre transmis au DMP et/ou &agrave; un ou plusieurs destinataire(s) via la MSSant&eacute;.</p>
<p>Le CREATEUR permet &eacute;galement &agrave; l&rsquo;utilisateur de pr&eacute;ciser&nbsp;les m&eacute;tadonn&eacute;es DMP/MSSant&eacute;&nbsp;: masquage au(x) PS, visibilit&eacute; au patient, visibilit&eacute; au(x) repr&eacute;sentant(s) l&eacute;gaux. Il permet &eacute;galement &agrave; l&rsquo;utilisateur de pr&eacute;ciser s&rsquo;il souhaite recevoir un accus&eacute; de r&eacute;ception DMP/MSSant&eacute; et/ou un accus&eacute; de lecture MSSant&eacute;.</p>
<p>Le GESTIONNAIRE r&eacute;ceptionne cette demande et utilise les informations port&eacute;es par la transaction ainsi que les informations contenues dans le(s) document(s) CDA pour r&eacute;aliser la transaction d&rsquo;alimentation du DMP et/ou l&rsquo;envoi vers le(s) destinataire(s) (Patient et/ou PS) via la MSSant&eacute; (i.e.&nbsp;; produire les m&eacute;tadonn&eacute;es XDS).</p>
<p>En fonction de la demande, le GESTIONNAIRE transmet au CREATEUR l&rsquo;accus&eacute; de r&eacute;ception DMP, l&rsquo;accus&eacute; de r&eacute;ception MSSant&eacute; et/ou l&rsquo;accus&eacute; de lecture MSSant&eacute;.</p>
<p>Dans le cas de la DrimBox, seule l&rsquo;alimentation du DMP avec le document de r&eacute;f&eacute;rence d&rsquo;objets d&rsquo;examen d&rsquo;imagerie (KOS) est r&eacute;alis&eacute;e. La DRIMBox-Source n&rsquo;est pas concern&eacute;e par la MSSant&eacute;.</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p>&nbsp;</p>

**(Note 1)** : _les systèmes référencés SEGUR vague 2 ne sont pas concernés
car, dans ce cas, le PDF est inclus dans une section du CDA Niv3._

### Processus collaboratif « Demande de remplacement de document(s) »

<div class="figure">
    <img src="image14.png" alt="Figure 10" title="Figure 10 : Processus collaboratif « Demande de remplacement de document(s) » pour publication sur DMP et envoi par MSSanté" style="width:100%;">
    <figcaption>Figure 10 : Processus collaboratif « Demande de remplacement de document(s) » pour publication sur DMP et envoi par MSSanté</figcaption>
</div>    
<br>

Le processus « Demande de remplacement de document(s) permet également
de gérer la mise à jour des métadonnées associées au(x) document(s). En
effet, la PFI, en authentification indirecte vis-à-vis du DMP, n'a pas
la possibilité d'utiliser la transaction « TD3.3 Gestion des attributs
d'un document » du profil Alimentation du DMP car celle-ci nécessite une
authentification directe.

Ainsi, dans le cas d'une demande de mise à jour des métadonnées de
masquage/démasquage aux PS et de visibilité du document au patient, une
nouvelle version de document est générée par le CREATEUR de documents.
Cette nouvelle version vient remplacer la précédente au niveau du
consommateur (DMP et/ou application métier destinatrice).

<table width="650">
<tbody>
<tr>
<td width="151">
<p><strong>Service Attendu</strong></p>
</td>
<td width="499">
<p>Le CREATEUR &eacute;met une demande de remplacement de document(s) vers le GESTIONNAIRE. Celui-ci r&eacute;alisera ensuite le relais vers le DMP pour r&eacute;aliser un Replace et vers MSSant&eacute; pour r&eacute;aliser un nouvel envoi contenant le(s) document(s) rempla&ccedil;ant le(s) document(s) initialement envoy&eacute;s.</p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Pr&eacute;-Conditions</strong></p>
</td>
<td width="499">
<p>Le document CDA doit &ecirc;tre disponible, valid&eacute; et identifi&eacute; comme rempla&ccedil;ant un document pr&eacute;c&eacute;demment envoy&eacute; par MSSant&eacute; et/ou publi&eacute; sur le DMP.</p>
<p>L&rsquo;INS du patient doit &ecirc;tre obligatoirement qualifi&eacute; dans le cas o&ugrave; le remplacement du document est demand&eacute; au niveau du DMP.</p>
<p>Une d&eacute;rogation valable jusqu&rsquo;&agrave; fin 2023, puis renouvelable jusqu&rsquo;&agrave; sa r&eacute;vocation qui sera indiqu&eacute;e dans les futures versions du r&eacute;f&eacute;rentiel socle MSSant&eacute;#2, permet d&rsquo;&eacute;changer un courriel par MSSant&eacute; en l&rsquo;absence d&rsquo;un INS qualifi&eacute;.</p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Post-Conditions</strong></p>
</td>
<td width="499">
<p>La nouvelle version de document est publi&eacute;e sur le DMP et envoy&eacute;e par MSSant&eacute; (Patient et/ou PS). L&rsquo;ancienne version de document est mise au statut &laquo;&nbsp;Deprecated&nbsp;&raquo; au niveau du CONSOMMATEUR MSSant&eacute; et/ou sur le DMP.</p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Contraintes fonctionnelles</strong></p>
</td>
<td width="499">
<p>Dans le cas o&ugrave; le CREATEUR de document(s) transmet les 2 formats de documents s&eacute;par&eacute;ment (CDA Niv1 et CDA Niv3), le remplacement (ou de la mise &agrave; jour des m&eacute;tadonn&eacute;es) d&rsquo;un des formats doit s&rsquo;accompagner du remplacement (ou de la mise &agrave; jour des m&eacute;tadonn&eacute;es) du format li&eacute;. La transaction doit contenir les 2 nouvelles versions de documents. Cf <em>Note 1</em></p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Sc&eacute;nario Nominal</strong></p>
</td>
<td width="499">
<p>Le CREATEUR transmet une demande de remplacement de document(s) au GESTIONNAIRE. Il peut s&rsquo;agir de mettre jour le document, de masquer/d&eacute;masquer le document aux PS, de rendre visible le document au patient ou de rendre visible le document aux repr&eacute;sentants l&eacute;gaux.</p>
<p>&nbsp;</p>
<p>Le GESTIONNAIRE r&eacute;ceptionne cette demande de remplacement et utilise les informations port&eacute;es par la transaction ainsi que les informations contenues dans le(s) document(s) CDA pour r&eacute;aliser la transaction d&rsquo;alimentation du DMP et/ou l&rsquo;envoi vers le(s) destinataire(s) (Patient et/ou PS) via la MSS (i.e.&nbsp;; produire les m&eacute;tadonn&eacute;es XDS).</p>
<p>Le code RPLC dans clinicalDocument/relatedDocument@typeCode dans le CDA-R2 <a href= https://esante.gouv.fr/sites/default/files/media_entity/documents/ci-sis_contenu_volet-structuration-minimale_v1.15.pdf> [cf: : volet CI-SIS : CONTENU_VOLET-STRUCTURATION-MINIMALE_V1.15]</a> permet de constituer l&rsquo;association RPLC dans la soumission XDS sur le DMP pour le remplacement <a href= https://industriels.sesam-vitale.fr> [cf: SESAM-VITALE : Service DMP intégré aux LPS - Version 2.10.0]</a>.</p>
<p><sup>&nbsp;</sup></p>
<p>En fonction de la demande, le GESTIONNAIRE transmet au CREATEUR l&rsquo;accus&eacute; de r&eacute;ception DMP, l&rsquo;accus&eacute; de r&eacute;ception MSSant&eacute; et/ou l&rsquo;accus&eacute; de lecture MSSant&eacute;.</p>
</td>
</tr>
</tbody>
</table>

**Note 1** : _les systèmes référencés SEGUR vague 2 ne sont pas concernés
car, dans ce cas, le PDF est inclus dans une section du CDA Niv3._

<blockquote class="stu-note">
    <p>
    <b>Point d'attention :</b> La mise à jour du document ou de ses métadonnées de masquage/visibilité a pour impact la création d'une nouvelle version du document avec un nouvel identifiant et une nouvelle séquence hash.
    </p>
</blockquote>

### Processus collaboratif « Demande de suppression de document(s) »

<div class="figure">
    <img src="image15.png" alt="Figure 11" title="Figure 11 : Processus collaboratif « Demande de suppression de document(s) » pour publication sur DMP et envoi par MSSanté" style="width:100%;">
    <figcaption>Figure 11 : Processus collaboratif « Demande de suppression de document(s) » pour publication sur DMP et envoi par MSSanté</figcaption>
</div>    
<br>

<table width="650">
<tbody>
<tr>
<td width="151">
<p><strong>Service Attendu</strong></p>
</td>
<td width="499">
<p>Le CREATEUR &eacute;met une demande de suppression de document(s) vers le GESTIONNAIRE. Celui-ci r&eacute;alisera ensuite le relais vers le DMP pour r&eacute;aliser un Delete et vers MSSant&eacute; pour r&eacute;aliser un nouvel envoi contenant le(s) document(s) &agrave; supprimer.</p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Pr&eacute;-Conditions</strong></p>
</td>
<td width="499">
<p>Le document a &eacute;t&eacute; envoy&eacute; pr&eacute;alablement pour soumission au DMP et/ou pour envoi par MSSant&eacute;.</p>
<p>L&rsquo;INS du patient doit obligatoirement &ecirc;tre qualifi&eacute; dans le cas o&ugrave; la suppression du document du DMP est demand&eacute;e.</p>
<p>Une d&eacute;rogation valable jusqu&rsquo;&agrave; fin 2023, puis renouvelable jusqu&rsquo;&agrave; sa r&eacute;vocation qui sera indiqu&eacute;e dans les futures versions du r&eacute;f&eacute;rentiel socle MSSant&eacute;#2, permet d&rsquo;&eacute;changer un courriel par MSSant&eacute; en l&rsquo;absence d&rsquo;un INS qualifi&eacute;.</p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Post-Conditions</strong></p>
</td>
<td width="499">
<p>Le document est supprim&eacute; du DMP (availabilityStatus = Deleted) <a href= https://esante.gouv.fr/sites/default/files/media_entity/documents/ci-sis_contenu_volet-structuration-minimale_v1.15.pdf> [cf: : volet CI-SIS : CONTENU_VOLET-STRUCTURATION-MINIMALE_V1.15]</a>
<p>TD3.3 (Supprimer un document) <a href= https://esante.gouv.fr/sites/default/files/media_entity/documents/ci-sis_contenu_volet-structuration-minimale_v1.15.pdf> [cf: : volet CI-SIS : CONTENU_VOLET-STRUCTURATION-MINIMALE_V1.15]</a>
<p>Le document est &eacute;galement supprim&eacute; au niveau de chacun des destinataire(s) de l&rsquo;envoi par MSS.</p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Contraintes fonctionnelles</strong></p>
</td>
<td width="499">
<p>Dans le cas o&ugrave; le CREATEUR de documents transmet les 2 formats de documents s&eacute;par&eacute;ment (CDA Niv1 et CDA Niv3), la suppression d&rsquo;un des formats doit s&rsquo;accompagner de la suppression du format li&eacute;. La transaction doit contenir les 2 formats de document &agrave; supprimer. Hors p&eacute;rim&egrave;tre SEGUR.</p>
</td>
</tr>
<tr>
<td width="151">
<p><strong>Sc&eacute;nario Nominal</strong></p>
</td>
<td width="499">
<p>Une erreur d&eacute;tect&eacute;e n&eacute;cessite la suppression du document sans qu&rsquo;il soit remplac&eacute; par une autre version (ex. erreur d&rsquo;association entre le CR et le patient).</p>
<p>Le CREATEUR transmet une demande de suppression de document(s) au GESTIONNAIRE.</p>
<p>Le GESTIONNAIRE r&eacute;ceptionne cette demande de suppression et utilise les informations port&eacute;es par la transaction ainsi que les informations contenues dans le(s) document(s) CDA pour r&eacute;aliser la transaction de suppression du document sur le DMP et/ou l&rsquo;envoi vers le(s) destinataire(s) (Patient et/ou PS) via la MSS (i.e.&nbsp;; produire les m&eacute;tadonn&eacute;es XDS).</p>
<p>Un message est envoy&eacute; par le GESTIONNAIRE vers le(s) destinataire(s) MSSant&eacute; indiquant dans le corps du mail que le document doit &ecirc;tre supprim&eacute;.</p>
<p><a href=https://esante.gouv.fr/sites/default/files/media_entity/documents/ci-sis_service_volet-echange-documents-sante_v1.8.pdf>cf :  volet Volet Echange des Documents de Santé 1.8</a>.</p>
<p>En fonction de la demande, le GESTIONNAIRE transmet au CREATEUR l&rsquo;accus&eacute; de r&eacute;ception DMP, l&rsquo;accus&eacute; de r&eacute;ception MSSant&eacute; et/ou l&rsquo;accus&eacute; de lecture MSSant&eacute;.</p>
</td>
</tr>
</tbody>
</table>