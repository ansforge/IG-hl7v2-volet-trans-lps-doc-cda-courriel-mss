Ci-dessous la matrice de gestion pour les échanges MSSanté suivant les OBX valorisés. Le tableau présente une liste exhaustive des combinaisons possibles des OBX pour l'échange MSSANTE. Les cas non représentés génèrent un message d'erreur.

<table>
<tbody>
<tr>
<td width="245">
<p><strong>Balises OBX&nbsp;: </strong></p>
</td>
<td width="404">
<p><strong>Echange MSSANTE&nbsp;: </strong></p>
</td>
</tr>
<tr>
<td width="245">
<p>MASQUE_PS&nbsp;: N</p>
<p>INVISIBLE_PATIENT&nbsp;: N</p>
<p>INVISIBLE_REP_LEGAUX : N</p>
<p>CONNEXION_SECRETE&nbsp;: N</p>
<p>MODIF_CONF_CODE&nbsp;: N ou Y</p>
<p>DESTDMP&nbsp;: N ou Y</p>
<p>DESTMSSANTEPS&nbsp;: Y<br /> DESTMSSANTEPAT&nbsp;: Y</p>
<p>ACK_RECEPTION&nbsp;: N ou Y</p>
<p>ACK_LECTURE_MSS&nbsp;: N ou Y</p>
</td>
<td width="404">
<p>Envoi du document sur la boite MSSant&eacute; du PS/organisation/BAL applicative du destinataire et du Patient</p>
</td>
</tr>
<tr>
<td width="245">
<p>MASQUE_PS&nbsp;: N</p>
<p>INVISIBLE_PATIENT&nbsp;: Y</p>
<p>INVISIBLE_REP_LEGAUX : N</p>
<p>CONNEXION_SECRETE&nbsp;: N</p>
<p>MODIF_CONF_CODE&nbsp;: N ou Y</p>
<p>DESTDMP&nbsp;: N ou Y</p>
<p>DESTMSSANTEPS&nbsp;: Y<br /> DESTMSSANTEPAT&nbsp;: N</p>
<p>ACK_RECEPTION&nbsp;: N ou Y</p>
<p>ACK_LECTURE_MSS&nbsp;: N ou Y</p>
</td>
<td width="404">
<p>Envoi du document sur la boite MSSant&eacute; du PS/organisation/BAL applicative du destinataire</p>
</td>
</tr>
<tr>
<td width="245">
<p>MASQUE_PS&nbsp;: Y ou N</p>
<p>INVISIBLE_PATIENT&nbsp;: N</p>
<p>INVISIBLE_REP_LEGAUX : N ou Y</p>
<p>CONNEXION_SECRETE&nbsp;: N</p>
<p>MODIF_CONF_CODE&nbsp;: N ou Y</p>
<p>DESTDMP&nbsp;: N</p>
<p>DESTMSSANTEPS&nbsp;: N<br /> DESTMSSANTEPAT&nbsp;: Y</p>
<p>ACK_RECEPTION&nbsp;: N ou Y</p>
<p>ACK_LECTURE_MSS&nbsp;: N ou Y</p>
</td>
<td width="404">
<p>Envoi du document sur la boite MSSant&eacute; du patient</p>
</td>
</tr>
</tbody>
</table>

**Lien entre l'EN-TETE CDA et les métadonnées XDS**

Une annexe disponible sur le CI-SIS indique la correspondance entre les données d'en-tête d'un document CDA définies dans le volet structuration minimale des documents de Santé et les métadonnées XDS définies dans le [volet partage de documents de Santé](https://esante.gouv.fr/sites/default/files/media_entity/documents/ci-sis_service_volet-partage-documents-sante_v1.15.pdf).

-   **[Annexe -- Lien Entre l'en-tête CDA et les métadonnées XDS](https://esante.gouv.fr/sites/default/files/media_entity/documents/CI-SIS_ANX_LIENS-CDA-METADONNEES-XDS_V1.6.pdf)**