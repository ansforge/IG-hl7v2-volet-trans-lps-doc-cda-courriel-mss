<p style="padding: 5px; border-radius: 5px; border: 2px solid maroon; background: #ffffe6; width: 65%">
<b>Brief description of this Implementation Guide</b><br>
[Add a brief description of this IG in English]
</p>

<!--  A décommenter lors de la publication -->

<div style="width: 65%">
    <blockquote class="stu-note">
    <p>
    <b>Attention !</b> Cet Implementation Guide n'est pas en version courante. La version officielle est ici :  <a href="https://esante.gouv.fr/volet-de-transmission-dun-document-cda-r2-en-hl7v2">https://esante.gouv.fr/volet-de-transmission-dun-document-cda-r2-en-hl7v2</a>
    </p>
    </blockquote>
</div>


<div class="figure">
    <img src="ci-sis-logo.png" alt="CI-SIS" title="Logo du CI-SIS" style="width:100%;">
</div>

### Avant-propos

Ce document fait partie de la couche Service du Cadre d'Interopérabilité des Systèmes d'Information de santé (CI_SIS).

<div style="width: 65%">
    <blockquote class="stu-note">
    <p>
    Cette version, au statut Trial Implementation, intègre le traitement des commentaires reçus par l’ANS pendant la phase de commentaires publics qui s’est déroulée du 27/11/2023 au 08/12/2023 ainsi que des corrections ou des améliorations apportées à la suite du projectathon organisé par l’ANS en septembre 2023. Cette version du volet intègre également le résultat de l’étude conduite en janvier 2024 par la DNS avec des industriels et leurs représentants sur les cas d’usage de la MSSanté présentés dans la section Volume 1 – Etude fonctionnelle.  
    </p>
    </blockquote>
</div>

Ce présent volet décrit la possibilité pour un logiciel métier d’une organisation de déléguer à un acteur tiers, la plateforme d’intermédiation (PFI), la capacité de traiter un courriel entrant provenant d’une BAL MSSanté et de générer à partir de ce courriel une demande d’intégration ou de remplacement ou de suppression d’un document clinique en direction de l’application métier consommatrice. Ce volet est à considérer par le lecteur en association avec un autre volet du CI_SIS, [le volet « Transmission de document(s) CDA en HL7v2 »](https://esante.gouv.fr/volet-de-transmission-dun-document-cda-r2-en-hl7v2) de façon à avoir une vision de bout en bout des échanges au travers de la MSSanté (du CREATEUR de la demande de traitement sur un document vers le CONSOMMATEUR final de cette demande).

Les deux volets en question intègrent à la fois une partie fonctionnelle et une partie technique.

La partie fonctionnelle décrit, à titre d’exemple et de façon non exhaustive, un ensemble de cas d’usage. Sur la base de ces cas d’usage, sont ensuite définis des acteurs du système d’information (au sens d’IHE) et des transactions qui interviennent entre ces acteurs pour répondre à ces cas d’usage. Les processus collaboratifs sont ensuite décrits et les flux entre les acteurs sont également identifiés.

La partie technique décrit les standards retenus pour implémenter les flux identifiés par l’étude fonctionnelle et décrit dans le détail les règles d’implémentation de ces standards.

Pour une meilleure compréhension du lecteur, les cas d’usage décrits dans la partie fonctionnelle de chacun des volets couvrent la totalité des échanges entre les acteurs définis dans les deux volets. Dans le contexte de ce présent document, seuls les échanges entre la PFI qui traite le courriel entrant et le logiciel métier consommateur font partie du périmètre du volet.

Dans le cas d’usage où la demande provenant du CREATEUR est relayée par le GESTIONNAIRE de l’établissement vers une BAL personnelle ou organisationnelle d’un autre établissement, l’envoi de l’accusé de lecture MSSanté (Message Disposition Notification- MDN décrit dans la [RFC 8098](https://datatracker.ietf.org/doc/html/rfc8098)) est déclenché par le traitement du courriel déposé dans la BAL de l’utilisateur destinataire (lecture, suppression, traitement, etc.). Le message MDN est alors réceptionné par la PFI de l’établissement expéditeur qui construit le message métier HL7 `ZAM^Z03^ZAM_Z01` et le transmet au logiciel métier de l’utilisateur expéditeur.

Une liste de cas d’usage, non exhaustive, est présentée à titre d’exemple dans le Volume 1 - Etude fonctionnelle, pour susciter les retours des industriels et des utilisateurs lors des prochains projectathons.


Rappel des conventions utilisées par IHE et HL7 :

<table>
<tbody>
<tr>
<td width="113">
<p><strong>Code d&rsquo;usage</strong></p>
</td>
<td width="510">
<p><strong>Signification</strong></p>
</td>
</tr>
<tr>
<td width="113">
<p>R</p>
</td>
<td width="510">
<p>Requis&nbsp;: l&rsquo;&eacute;l&eacute;ment de donn&eacute;e doit obligatoirement &ecirc;tre renseign&eacute; par l&rsquo;&eacute;metteur et int&eacute;gr&eacute; par le r&eacute;cepteur</p>
</td>
</tr>
<tr>
<td width="113">
<p>RE</p>
</td>
<td width="510">
<p>Requis si connu&nbsp;: le syst&egrave;me doit d&eacute;montrer sa capacit&eacute; &agrave; renseigner l&rsquo;&eacute;l&eacute;ment en &eacute;mission et/ou &agrave; l&rsquo;exploiter en r&eacute;ception.</p>
<p>Sur le terrain il peut exister des situations o&ugrave; l&rsquo;&eacute;l&eacute;ment est non renseign&eacute;.</p>
</td>
</tr>
<tr>
<td width="113">
<p>O</p>
</td>
<td width="510">
<p>Optionnel</p>
</td>
</tr>
<tr>
<td width="113">
<p>X</p>
</td>
<td width="510">
<p>Non support&eacute;</p>
</td>
</tr>
<tr>
<td width="113">
<p>C</p>
</td>
<td width="510">
<p>Conditionnel&nbsp;: La condition de remplissage de l&rsquo;&eacute;l&eacute;ment de donn&eacute;e est sp&eacute;cifi&eacute;e dans le tableau de description du profil de message ou dans une note en dessous du tableau.</p>
</td>
</tr>
</tbody>
</table>

<table>
<tbody>
<tr>
<td width="113">
<p><strong>Code d&rsquo;usage</strong></p>
</td>
<td width="510">
<p><strong>Signification</strong></p>
</td>
</tr>
<tr>
<td width="113">
<p>[ ]</p>
</td>
<td width="510">
<p>Champ optionnel</p>
</td>
</tr>
<tr>
<td width="113">
<p>{ }</p>
</td>
<td width="510">
<p>Champ r&eacute;p&eacute;table</p>
</td>
</tr>

<tr>
<td width="113">
<p>[{ }]</p>
</td>
<td width="510">
<p>Champ optionnel et r&eacute;p&eacute;table</p>
</td>
</tr>
</tbody>
</table>

<div class="draft-content">
<p>
<b>QUESTIONS OUVERTES :</b><br>
<a href="https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/discussions/3">LPS_MSS_Q1 :</a> demande de fusionner les deux spécifications : Transmission d’un document CDA en HL7v2 et Transmission au LPS d’un document CDA provenant d’un courriel. La fusion des deux spécifications est sans doute possible. Cependant, utiliser la même transaction entre les acteurs CREATEUR/GESTIONNAIRE et GESTIONNAIRE/CONSOMMATEUR nécessite d’effectuer une étude plus approfondie de façon à déterminer comment harmoniser ces transactions. La mise en place d'une transaction unique indépendamment du contexte créerait de l'ambiguïté avec notamment des informations non pertinentes véhiculées entre le GESTIONNAIRE et le CONSOMMATEUR (alimentation DMP, échange MSSanté…).
<br><br>
<a href="https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/discussions/4">LPS_MSS_Q2 :</a> demande d’un éditeur de permettre également d’utiliser le message ORU (HL7v2.5) de la même façon que le message MDM pour transférer la demande portée par le courriel reçu par le GESTIONNAIRE vers l’acteur CONSOMMATEUR. Un sondage a été proposé aux éditeurs sur ce sujet. Ce sondage n’a pas permis de dégager un consensus clair sur ce point (50% de non et 50% de oui et d’autre part l’éditeur à l’origine de la demande n’a pas confirmé ce besoin au niveau du sondage.
</p>
</div>

### Introduction
Ce document présente les spécifications techniques du volet « Transmission au LPS d’un document CDA provenant d'un courriel MSSanté ». Ces spécifications permettent la transmission d’une demande de traitement concernant un document clinique au format CDA-R2 (Clinical Document Architecture) (demande d’intégration/de remplacement/de suppression d’un document)) entre la Plateforme d’Intermédiation (PFI) de l’établissement et le logiciel du professionnel de santé (LPS) destinataire après détection d’un courriel dans une Boîte Aux Lettres (BAL) applicative MSSanté accessible par la PFI.

La PFI extrait les documents médicaux de l’archive du courriel MSSanté reçue puis les transmet unitairement au logiciel de professionnel de santé (LPS) consommateur. Le LPS acquitte ensuite la réception des informations portées par la transaction.

#### Dépendances documentaires

Cette spécification n’est pas autonome.
Le lecteur pourra également consulter le volet « [Transmission de document(s) CDA en HL7v2](https://esante.gouv.fr/volet-de-transmission-dun-document-cda-r2-en-hl7v2) » du CI_SIS pour avoir une vision complète et transversale des échanges représentée de façon synthétique sur la figure suivante et décrits de façon détaillée dans le volume 2 du présent document :


<div class="figure" style='text-align: center;'>
    <img src="image7.png" alt="Figure 1" title="Figure 1 : Représentation synthétique des échanges et articulation entre les deux volets du CI_SIS" style="width:80%;">
    <figcaption><b>Figure 1 : Représentation synthétique des échanges et articulation entre les deux volets du CI_SIS</b></figcaption>
</div>
<br>


##### Dépendances avec la documentation SEGUR

Ce document doit être utilisé dans le cadre du référencement SEGUR vague 2. Il s’applique, entre autres, à la vague 2 du Ségur Numérique mais pas uniquement. Il peut également être utilisé hors SEGUR.

##### Positionnement dans le cadre d'interopérabilité

Cette spécification n’est pas autonome. Les développeurs doivent également connaître et maîtriser d’autres volets du CI_SIS publiés par l’ANS :

-   [Le volet Echange de documents de santé](https://esante.gouv.fr/sites/default/files/media_entity/documents/ci-sis_service_volet-echange-documents-sante_v1.8.pdf),

Ainsi que le [Référentiel Socle MSSanté #2, Clients messagerie de sécurité de santé version 1.0.1](https://esante.gouv.fr/espace_documentation/mssante-clients-de-messageries-securisees-de-sante/referentiel-socle-mssante-2/actual), publié par l’ANS.

#### Ce dont ne traite pas ce volet du CI_SIS

Les contraintes de sécurité concernant les flux échangés ne sont pas traitées dans ce document. En effet, les aspects relatifs à la sécurité sont du ressort du système d’information les implémentant.
Ce volet du CI_SIS n’a pas vocation à décrire le cadre juridique applicable. Il appartient à chaque acteur concerné par ce volet de veiller à ce que les fonctionnalités fournies et/ou mises en œuvre respectent ce cadre légal, notamment en termes de confidentialité et de sécurité des données par application des règles de la [PGSSI_S](https://esante.gouv.fr/produits-services/pgssi-s).

#### Lectorat cible

Ce document s'adresse aux développeurs des interfaces interopérables des systèmes implémentant le volet « Transmission au LPS d’un document CDA provenant d'un courriel MSSanté » ou à toute autre personne intervenant dans le processus de mise en place de ces interfaces.

<!-- ### Auteurs et contributeurs

| Role  | Nom | Organisation | Contact |
| --- | --- | --- | --- |
| **Primary Editor** | Prenom Nom | Agence du Numérique en Santé | prenom.nom@address.email | -->