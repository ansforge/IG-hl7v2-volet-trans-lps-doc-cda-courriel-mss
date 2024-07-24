### Liste des Acteurs et systèmes concernés

Le présent volet met en œuvre les Acteurs IHE suivants, représentant le rôle joué par un ou plusieurs composants du système d’information :

<table>
<tbody>
<tr>
<td width="217">
<p><strong>Acteur&nbsp;:</strong></p>
</td>
<td width="432">
<p><strong>Description&nbsp;:</strong></p>
</td>
</tr>
<tr>
<td width="217">
<p>GESTIONNAIRE</p>
</td>
<td width="432">
<p>Le GESTIONNAIRE r&eacute;ceptionne et transmet au syst&egrave;me CONSOMMATEUR les demandes de transmission initiale/remplacement/suppression de document(s) provenant d&rsquo;un courriel.</p>
</td>
</tr>
<tr>
<td width="217">
<p>CONSOMMATEUR</p>
</td>
<td width="432">
<p>Le CONSOMMATEUR r&eacute;ceptionne et g&egrave;re les demandes de transmission initiale/remplacement/suppression de document(s) issues d&rsquo;un courriel, provenant du syst&egrave;me GESTIONNAIRE et renvoie l&rsquo;accus&eacute; de traitement de la demande vers le GESTIONNAIRE.</p>
</td>
</tr>
</tbody>
</table>

Le tableau suivant liste, pour chacun des acteurs, les systèmes du SIH concernés :

<table>
<tbody>
<tr>
<td width="141">
<p><strong>Acteur&nbsp;:</strong></p>
</td>
<td width="508">
<p><strong>Syst&egrave;mes concern&eacute;s&nbsp;:</strong></p>
</td>
</tr>
<tr>
<td width="141">
<p><strong>&nbsp;</strong></p>
</td>
<td width="508">
<p><strong>&nbsp;</strong></p>
</td>
</tr>
<tr>
<td width="141">
<p>GESTIONNAIRE</p>
</td>
<td width="508">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Les Plateformes d&rsquo;Interm&eacute;diation (PFI) qui assurent la transmission de document(s) cliniques provenant d&rsquo;un courriel MSSant&eacute; vers un CONSOMMATEUR (le LPS destinataire).</p>
</td>
</tr>
<tr>
<td width="141">
<p>CONSOMMATEUR</p>
</td>
<td width="508">
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Tout logiciel m&eacute;tier (LPS) du SIH qui r&eacute;cup&egrave;re et g&egrave;re la demande de traitement du document transmis par le GESTIONNAIRE.</p>
<p>-&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Dans le contexte du SEGUR vague 2, les applications consommatrices de ces documents sont limit&eacute;es au dossier patient informatis&eacute; (DPI) et au syst&egrave;me de gestion de radiologie (RIS).</p>
</td>
</tr>
</tbody>
</table>

### Diagramme des Acteurs/Transactions

<div class="figure" style='text-align: center;'>
    <img src="image14.png" alt="Figure 7" title="Figure 7 : Diagramme des Acteurs/transactions" style="width:80%;">
    <figcaption><b>Figure 7 : Diagramme des Acteurs/transactions</b></figcaption>
</div>    
<br>

Le tableau ci-dessous représente l’ensemble des acteurs directement impliqués dans ce volet ainsi que les transactions entre ces acteurs.
Pour être en conformité avec ce volet, chaque acteur doit supporter les transactions obligatoires (R-Required) et peut supporter les transactions optionnelles (O-Optional).

<table>
<tbody>
<tr>
<td width="131">
<p><strong>Acteur</strong></p>
</td>
<td width="323">
<p><strong>Transaction</strong></p>
</td>
<td width="189">
<p><strong>Caract&egrave;re requis/optionnel</strong></p>
</td>
</tr>
<tr>
<td width="131">
<p>GESTIONNAIRE</p>
</td>
<td width="323">
<p>Flux6 HL7-MDM en &eacute;mission : Demande de transmission/remplacement/suppression d&rsquo;un document CDA</p>
</td>
<td width="189">
<p>R</p>
</td>
</tr>
<tr>
<td width="131">
<p>CONSOMMATEUR</p>
</td>
<td width="323">
<p>Flux6 HL7-MDM en r&eacute;ception : Demande de transmission/remplacement/suppression d&rsquo;un document CDA</p>
</td>
<td width="189">
<p>R</p>
</td>
</tr>
</tbody>
</table>

### Regroupement requis des Acteurs

Cette section décrit les exigences en termes de regroupement d’acteurs pour chacun des acteurs identifiés précédemment.

<table>
<tbody>
<tr>
<td width="216">
<p><strong>Acteur de ce volet</strong></p>
</td>
<td width="216">
<p><strong>Group&eacute; avec un autre acteur</strong></p>
</td>
<td width="217">
<p><strong>R&eacute;f&eacute;rence</strong></p>
</td>
</tr>
<tr>
<td width="216">
<p>GESTIONNAIRE</p>
</td>
<td width="216">
<p>Syst&egrave;me cible (Portable Media Importer) XDM</p>
</td>
<td width="217">
<p><a href="https://esante.gouv.fr/sites/default/files/media_entity/documents/ci-sis_service_volet-echange-documents-sante_v1.8.pdf">Volet Echange de documents de sant&eacute;</a></p>
</td>
</tr>
<tr>
<td width="216">
<p>CONSOMMATEUR</p>
</td>
<td width="216">
<p>Content Consumer (TF PCC<a href="#_ftn1" name="_ftnref1">[1]</a>)</p>
</td>
<td width="217">
<p>TF Patient Care Coordination &ndash; Appendix A: Actors definition</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p><a href="#_ftnref1" name="_ftn1">[1]</a> PCC&nbsp;: <a href="https://www.ihe.net/uploadedFiles/Documents/PCC/IHE_PCC_TF_Vol1.pdf">Patient Care Coordination &ndash; Appendix A&nbsp;: Actors definition</a></p>

L'acteur GESTIONNAIRE est groupé avec :

-   L'acteur Système cible du volet *d'Echange de documents de santé*, pour permettre à la PFI de réceptionner l'archive IHE_XDM inclue dans le courriel reçu de l'extérieur,

L'acteur CONSOMMATEUR est groupé avec :

-   L'acteur Content Consumer définit dans le Technical Framework PCC d'IHE, permettant au CONSOMMATEUR de visualiser et d'importer tout ou parties du document CDA.
