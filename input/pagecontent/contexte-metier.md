#### Les groupes de processus

Réception par la plateforme d'intermédiation (PFI) d'une demande de traitement sur le(s) document(s) clinique(s) relatif(s) à un patient provenant d'un logiciel métier de l'établissement, pour publication ensuite vers le DMP et/ou envoi par MSSanté vers un ou plusieurs destinataire(s). Ce groupe de processus est divisé en quatre processus décrits dans les sections suivantes.

#### Les processus

Le groupe de processus est divisé en quatre processus :

-   Une demande de transmission initiale de document(s) pour publication sur le DMP et/ou envoi par MSSanté,

-   Une demande de remplacement de document(s) initialement publié(s) sur le DMP et/ou initialement envoyé(s) par MSSanté,

-   Une demande de mise à jour des métadonnées de document(s)^(\*)^ initialement publié(s) sur le DMP et/ou initialement envoyé(s) par MSSanté,

-   Une demande de suppression de document(s) initialement publié(s) sur le DMP et/ou initialement envoyé(s) par MSSanté.

(\*) : _dans le contexte français, conformément au volet *Partage de documents de santé* du CI_SIS, la mise à jour des métadonnées du document est limitée à la mise à jour des informations de masquage du document aux PS et de mise en visibilité du document au patient et à ses représentants légaux ainsi que le statut du document._

La PFI interagissant avec le DMP en mode d'authentification indirecte, il lui est impossible de mettre en œuvre la transaction TD3.3 (Gestion des attributs d'un document) du profil Alimentation du DMP, décrite dans le *Guide d'implémentation du DMP* (transaction équivalente à la
transaction Update Document Set \[[ITI-57](https://profiles.ihe.net/ITI/TF/Volume2/ITI-57.html)\] du profil IHE Update Metadata), car celle-ci nécessite une authentification directe (cf la matrice des droits fonctionnels du DMP).

Dans ce contexte, la mise à jour des métadonnées de masquage/démasquage aux PS et de visibilité du document au patient sera gérée comme un remplacement de document, ce qui implique la création d'une nouvelle version de document par le système créateur de documents. Cette nouvelle version vient remplacer la précédente au niveau du consommateur (DMP ou logiciel métier destinataire du courriel).

Le nombre de processus est ainsi réduit aux trois processus synthétisés sur la Figure 6.

<div class="figure">
    <img src="image11.png" alt="Figure 6" title="Figure 6 : Organisation du contexte métier du volet « Transmission de documents CDA en HL7v2 »" style="width:100%;">
    <figcaption>Figure 6 : Organisation du contexte métier du volet « Transmission de documents CDA en HL7v2 »</figcaption>
</div>    
<br>

Le périmètre de l'étude englobe les processus en bleu sur le diagramme de paquetage.