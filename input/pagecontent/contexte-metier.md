##### Les groupes de processus

Réception par la plateforme d’intermédiation (PFI) d’une demande de traitement sur le(s) document(s) clinique(s) relatif(s) à un patient provenant d’une Boîte aux Lettres (BAL) MSSanté, pour transmission et traitement de cette demande au niveau d’un logiciel consommateur au sein de l’établissement. Ce groupe de processus est divisé en quatre processus décrits dans les sections suivantes.

##### Les processus

Le groupe de processus est divisé en quatre processus :

-   Une demande de transmission initiale de document(s) pour intégration dans le LPS,

-   Une demande de remplacement de document(s) initialement envoyé(s) par MSSanté pour remplacement au niveau du LPS,

-   Une demande de mise à jour des métadonnées de document(s)(\*) initialement envoyé(s) par MSSanté pour mise à jour au niveau du LPS,

-   Une demande de suppression de document(s) initialement envoyé(s) par MSSanté pour suppression au niveau du LPS.

(\*) : _dans le contexte français, conformément au [volet Partage de
documents de santé du CI_SIS](https://esante.gouv.fr/volet-partage-de-documents-de-sante), la mise à jour des métadonnées du document est limitée à la mise à jour des informations de masquage du document aux PS et de mise en visibilité du document au patient et à ses représentants légaux ainsi que le statut du document._

_Cette mise à jour est gérée comme un remplacement de document, ce qui implique la création d'une nouvelle version de document par le système créateur de documents. Cette nouvelle version vient remplacer la précédente au niveau du consommateur (logiciel métier destinataire du courriel)._



Le nombre de processus est ainsi réduit aux trois processus synthétisés sur la Figure suivante.

Dans le contexte du SEGUR vague 2, les applications consommatrices de ces documents sont limitées au dossier patient informatisé (DPI) et au système de gestion de radiologie (RIS).

<div class="figure" style='text-align: center;'>
    <img src="image13.png" alt="Figure 6" title="Figure 6 : Organisation du contexte métier du volet « Transmission au LPS d'un document provenant d'un courriel »" style="width:60%;">
    <figcaption><b>Figure 6 : Organisation du contexte métier du volet « Transmission au LPS d'un document provenant d'un courriel »</b></figcaption>
</div>    
<br>

Le périmètre de l'étude englobe les processus en bleu sur le diagramme de paquetage.