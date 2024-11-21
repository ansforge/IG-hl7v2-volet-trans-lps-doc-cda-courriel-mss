
### Historique du volet au format guide d'implémentation

#### version 1.1.1

**Version mineure sans impact sur le développement (changement de format, corrections de typo, précisions ou ajout d'informations)**

* Modification du format du volet : passage du format PDF au format guide d'implémentation ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
* Avant-propos : suppression d’une ligne vide du tableau des conventions HL7, IHE ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
* Ensemble du document :
  * remplacement de message MDN par MDN (qui signifie d’emblée Message Disposition Notification) ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
* Volume 1 Etude fonctionnelle
  * remplacement du terme « section » par « volume 2 » ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
  * [processus de transmission initiale de document(s)](def-proc-collab.html#processus-collaboratif-demande-de-transmission-initiale-de-documents) : scénario nominal, remplacement « demande de traitement de(s) document(s) » par « demande d’intégration du document » ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
  * [processus de suppression de document(s)](def-proc-collab.html#processus-collaboratif-demande-de-suppression-de-documents) : scénario nominal, remplacement « demande de suppression de(s) document(s) » par « demande de suppression du document » ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
* Volume 2 Etude technique
  * [Choix des standards](volume2.html#choix-des-standards) : suppression de la phrase « Les échanges MSSanté doivent prendre en compte les restrictions positionnées sur le message. (Exemple : un document avec un masquage Médecin ne doit pas être envoyé sur le mail MSSanté du médecin). » qui n’a pas de rapport avec le choix des standards. ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
  * correction typos/cohérence pour le type message en MSH-9.3 dans les [profils des messages](profils-messages.html#eléments-de-contrôle-du-message-mdm) ([6](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/issues/6))
  * [description fonctionnelle du message MDM](profils-messages.html#description-fonctionnelle-du-message-mdm) : correction dans la figure de la cardinalité [5..*] par [4..*] de l’OBX portant les métadonnées DMP/MSS ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
  * [Document Masqué aux professionnels de Santé](profils-messages.html#document-masqué-aux-professionnels-de-santé) : métadonnée de masquage aux PS : Ajout de la valeur manquante Y (YES) ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
  * Correction description des segments PRT pour 'destinataire' et 'adresse mail de réponse' dans les [profils des messages](profils-messages.html#le-groupe-de-segments-obxnte-portant-le-document-cda) [(9)](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/issues/9)
  * 
  * Déplacement de la section LIEN ENTRE L’EN-TETE CDA ET LES METADONNEES XDS dans Volume 3 Annexes ([8](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/issues/8))
* Volume 3 Annexes
  * [Structure du MDN (MSSanté)](struct-msg-mdn.html) (Annexe 4) modification du titre : Structure du MDN (Message Disposition Notification) - MSSanté ([2](https://github.com/ansforge/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/pull/2))
  * [exemples de messages d’acquittement](profils-messages.html#exemple)
    * Correction de MSH-21 (version de l’interface 1.1 au lieu de 1.2) sur le segment MSH du message initial MDM
    * Suppression du champ MSH-21 (le message d’acquittement n’a pas de contraintes particulières par rapport au message spécifié dans le standard international)

### Rappel de l'historique du volet des anciennes versions au format PDF (avant novembre 2024)

Ici nous rappelons l'historique des précédentes versions.
Cet historique est également disponible dans la dernière version du volet au format pdf : [ANNEXE 7 CI_SIS_TRANS_LPS_DOC_CDA_COURRIEL_MSSANTE_V1.1_Post_PAT_2023_CONCERTATION_FINAL.pdf](https://esante.gouv.fr/sites/default/files/media_entity/documents/CI_SIS_TRANS_LPS_DOC_CDA_COURRIEL_MSSANTE_V1.1_Post_PAT_2023_CONCERTATION_FINAL.pdf)

<table class="MsoNormalTable" border="1" cellspacing="0" cellpadding="0" width="100%" style="width:100.66%;margin-left:-3.1pt;border-collapse:collapse;border:none">
 <tbody><tr style="height:15.9pt">
  <td style="border:none;padding:0cm 0cm 0cm 0cm" width="0%"><p class="MsoNormal">&nbsp;</p></td>
  <td width="10%" colspan="2" style="width:10.68%;border:solid gray 1.0pt;
  background:#D9D9D9;padding:2.85pt 2.85pt 2.85pt 2.85pt;height:15.9pt">
  <p class="MsoNormal" style="margin-bottom:0cm"><b><span style="color:black">Version</span></b></p>
  </td>
  <td width="29%" colspan="4" style="width:29.6%;border:solid gray 1.0pt;
  border-left:none;background:#D9D9D9;padding:2.85pt 2.85pt 2.85pt 2.85pt;
  height:15.9pt">
  <p class="MsoNormal" style="margin-bottom:0cm"><b><span style="color:black">Rédigé
  par</span></b></p>
  </td>
  <td width="29%" colspan="4" style="width:29.58%;border:solid gray 1.0pt;
  border-left:none;background:#D9D9D9;padding:2.85pt 2.85pt 2.85pt 2.85pt;
  height:15.9pt">
  <p class="MsoNormal" style="margin-bottom:0cm"><b><span style="color:black">Vérifié
  par</span></b></p>
  </td>
  <td width="29%" colspan="3" style="width:29.5%;border:solid gray 1.0pt;
  border-left:none;background:#D9D9D9;padding:2.85pt 2.85pt 2.85pt 2.85pt;
  height:15.9pt">
  <p class="MsoNormal" style="margin-bottom:0cm"><b><span style="color:black">Validé
  par</span></b></p>
  </td>
 </tr>
 <tr>
  <td style="border:none;padding:0cm 0cm 0cm 0cm" width="0%"><p class="MsoNormal">&nbsp;</p></td>
  <td width="10%" colspan="2" rowspan="2" style="width:10.68%;border:solid gray 1.0pt;
  border-top:none;padding:2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" align="center" style="margin-bottom:0cm;text-align:center">1.0</p>
  </td>
  <td width="14%" colspan="2" style="width:14.78%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">Kereval</p>
  </td>
  <td width="14%" colspan="2" style="width:14.82%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">Le 13/02/2023</p>
  </td>
  <td width="14%" colspan="2" style="width:14.78%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">ANS</p>
  </td>
  <td width="14%" colspan="2" style="width:14.82%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">Le 19/02/2023</p>
  </td>
  <td width="14%" colspan="2" style="width:14.8%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">ANS</p>
  </td>
  <td width="14%" style="width:14.7%;border-top:none;border-left:none;
  border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">Le 26/04/2023</p>
  </td>
 </tr>
 <tr>
  <td style="border:none;padding:0cm 0cm 0cm 0cm" width="0%"><p class="MsoNormal">&nbsp;</p></td>
  <td width="88%" colspan="11" style="width:88.66%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">Motif et nature de la
  modification&nbsp;: <b>Première version </b></p>
  </td>
 </tr>
 <tr>
  <td style="border:none;padding:0cm 0cm 0cm 0cm" width="0%"><p class="MsoNormal">&nbsp;</p></td>
  <td width="10%" colspan="2" rowspan="2" style="width:10.68%;border:solid gray 1.0pt;
  border-top:none;padding:2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" align="center" style="margin-bottom:0cm;text-align:center">1.1</p>
  </td>
  <td width="14%" colspan="2" style="width:14.78%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">ANS</p>
  </td>
  <td width="14%" colspan="2" style="width:14.82%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">Le 24/10/2023</p>
  </td>
  <td width="14%" colspan="2" style="width:14.78%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">ANS</p>
  </td>
  <td width="14%" colspan="2" style="width:14.82%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">&nbsp;</p>
  </td>
  <td width="14%" colspan="2" style="width:14.8%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">ANS</p>
  </td>
  <td width="14%" style="width:14.7%;border-top:none;border-left:none;
  border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">&nbsp;</p>
  </td>
 </tr>
 <tr>
  <td style="border:none;border-bottom:solid gray 1.0pt" width="0%"><p class="MsoNormal">&nbsp;</p></td>
  <td width="88%" colspan="11" style="width:88.66%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:36.0pt;text-indent:-18.0pt"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Ajout
  de la partie Avant-propos et des questions ouvertes</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:36.0pt;text-indent:-18.0pt"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Le
  volet est scindé en 2 parties&nbsp;: Etude fonctionnelle et Etude technique</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:36.0pt;text-indent:-18.0pt"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Section
  1&nbsp;: suppression de toutes références au choix technique (HL7)</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:36.0pt;text-indent:-18.0pt"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Ajout
  de l’étude fonctionnelle</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  2&nbsp;: Cas d’usage</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  3&nbsp;: Organisation métier</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  4&nbsp;: Acteurs et Transactions</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  5&nbsp;: cas d’usage</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  6&nbsp;: Définition des processus collaboratifs</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  7&nbsp;: Identification des flux.</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:36.0pt;text-indent:-18.0pt"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Etude
  technique</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  7&nbsp;: Périmètre. </p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp; </span></span>Précision
  concernant l’accusé de lecture proposé à titre expérimental <span style="font-family:Wingdings">à</span> retours des éditeurs attendus.</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  8&nbsp;: ajout du rôle des acteurs</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  9&nbsp;: Standards</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp; </span></span>Référence la
  version 1.7.4 des «&nbsp;Contraintes sur les types de données HL7 v2.5 applicables
  aux profils d’intégration du cadre technique IT Infrastructure dans le périmètre
  d’IHE France&nbsp;» qui intègre l’agrandissement du champ EI-1 du type de
  données EI (passage de EI-1 à 199).</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp; </span></span>Ajout de la
  contrainte sur les types de données CE et CWE&nbsp;pré adoptée de la version
  2.7 d’HL7&nbsp;: nécessité de citer le code et le codeSystem dont est issu ce
  code.</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  11&nbsp;: Interactions entre les acteurs, précisions apportées sur le schéma</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  12.1.1&nbsp;: ajout du profil de message MDM</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  12.1.2&nbsp;: description fonctionnelle. </p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp; </span></span>Préciser la
  cardinalités sur les métadonnées [1..*]</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp; </span></span>1° OBXNTE&nbsp;:
  supprimer la référence au CDAr2 Niv1 (MDM contient un CDA Niv1 ou Niv3)</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  12.2.1&nbsp;: ajout des contraintes sur les éléments de contrôle MSH, MSA,
  ERR</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  12.2.2&nbsp;: éléments concernant le patient PID, PV1</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  12.2.3&nbsp;: Ajout de la description OCR</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  12.2.4&nbsp;: Ajout de la description du segment OBR</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  12.2.5&nbsp;: Ajout de la description du segment TXA</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  12.2.6&nbsp;: Eléments concernant la demande de traitement sur le document</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp; </span></span>12.2.6.1&nbsp;: Le1°
  groupe de segment OBXNTE, les segments et les champs sont à renseigner dans
  l’ordre indiqué. Ajout OBX-3.3 (contrainte CWE). Reprise des champs
  concernant l’expéditeur et le destinataire.</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp; </span></span>12.2.6.3&nbsp;:
  groupe de segment portant les métadonnées. </p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:144.0pt;text-indent:-18.0pt"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Les
  métadonnées doivent obligatoirement être renseignées et doivent apparaître
  dans l’ordre indiqué. </p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:144.0pt;text-indent:-18.0pt"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Ajout
  des lignes OBX-3.3 pour prendre en compte la contrainte sur le type de donnée
  CWE (code+codeSystem dont est issu le code)</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp; </span></span>Section 12.2.7.3&nbsp;:
  description ERR et exemples</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp; </span></span>Section
  12.3.1&nbsp;: description de l’évènement déclenchant de l’accusé de lecture
  dans le contexte de ce volet. Proposition de considérer cet accusé de lecture
  à titre expérimental <span style="font-family:Wingdings">à</span> retours des
  éditeurs attendus.</p>
  </td>
 </tr>
 <tr>
  <td width="11%" colspan="3" rowspan="2" style="width:11.28%;border:solid gray 1.0pt;
  border-top:none;padding:2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" align="center" style="margin-bottom:0cm;text-align:center">1.1</p>
  </td>
  <td width="14%" colspan="2" style="width:14.78%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">ANS</p>
  </td>
  <td width="14%" colspan="2" style="width:14.82%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">Le 15/01/2024</p>
  </td>
  <td width="14%" colspan="2" style="width:14.78%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">ANS</p>
  </td>
  <td width="14%" colspan="2" style="width:14.82%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">19/01/2024</p>
  </td>
  <td width="14%" colspan="2" style="width:14.8%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">DNS</p>
  </td>
  <td width="14%" style="width:14.7%;border-top:none;border-left:none;
  border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">21/02/2024</p>
  </td>
 </tr>
 <tr>
  <td width="88%" colspan="11" style="width:88.66%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="MsoNormal">Motif et nature de la modification&nbsp;: Prise en compte
  des retours de concertation publique (27/11/2023 au 08/12/2023) et prise en
  compte des modifications demandées par la DNS après clôture de la période de
  concertation publique.</p>
  <p class="MsoListParagraphCxSpFirst" style="margin-bottom:8.0pt;text-indent:
  -18.0pt;line-height:107%"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Rédaction
  des questions ouvertes</p>
  <p class="MsoListParagraphCxSpMiddle" style="margin-bottom:8.0pt;text-indent:
  -18.0pt;line-height:107%"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Section
  1.1&nbsp;: référence au volet Transmission d’un document CDA provenant d’un
  courriel MSS de façon à mettre en exergue le lien entre le présent volet et
  le volet référencé</p>
  <p class="MsoListParagraphCxSpMiddle" style="margin-bottom:8.0pt;text-indent:
  -18.0pt;line-height:107%"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Volume
  1 – Etude fonctionnelle</p>
  <p class="MsoListParagraphCxSpLast" style="margin-top:0cm;margin-right:0cm;
  margin-bottom:8.0pt;margin-left:72.0pt;text-indent:-18.0pt;line-height:107%"><span style="font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span>Section 2&nbsp;: complétude des cas d’usage DNS et
  modifications en fonction des remarques de la DNS</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  4.1&nbsp;: liste des acteurs concernés. L’envoi par le CONSOMMATEUR et la réception
  par le GESTIONNAIRE de l’accusé métier de lecture est supprimé (ZAM_Z03). Le
  GESTIONNAIRE envoie simplement l’accusé du message HL7 MDM. Cet accusé HL7
  rend compte du bon déroulement ou pas de la demande de traitement du document
  au niveau du CONSOMMATEUR.</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  4.2&nbsp;: Diagramme des acteurs/transactions. Suppression de l’accusé de
  lecture MSS (ZAM_Z03) entre l’acteur CONSOMMATEUR et l’acteur GESTIONNAIRE</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  4.3&nbsp;: regroupement de l’acteur CONSOMMATEUR avec l’acteur IHE Content
  Consumer</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  5&nbsp;: Processus collaboratifs. Amélioration de la rédaction des processus
  et suppression de la notion d’accusé métier de lecture MSS (ZAM_Z03).</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:36.0pt;text-indent:-18.0pt"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><span style="font-size:10.0pt;line-height:115%">Volume 2 – Etude technique</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  7&nbsp;: Périmètre de la transaction, suppression de l’accusé métier de
  lecture MSS (ZAM_Z03). L’accusé de lecture (message MDN) est généré par le
  GESTIONNAIRE sur réception de l’ack HL7 du message MDM </span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  9&nbsp;: Choix des standards</span></p>
  <p class="MsoListParagraph" style="margin-top:0cm;margin-right:0cm;margin-bottom:
  8.0pt;margin-left:108.0pt;text-indent:-18.0pt;line-height:107%"><span style="line-height:107%;font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;
  </span></span><span style="line-height:107%">Référencement de la version 2.11
  de la version française PAM.FR</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp; </span></span><span style="font-size:10.0pt;line-height:115%">Référencement de la version 1.8 des
  types de données HL7 en France (passage de la longueur du champ ED-1 de 16
  caractères à 128 caractères</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  11&nbsp;: modification de la figure 13. La PFI génère le message MDN
  (MSSanté) à partir de l’ack du message HL7 MDM. Le client de messagerie de la
  PFI envoi cet accusé de lecture (message MDN MSSanté) à l’expéditeur.</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  12.2.6.1&nbsp;: OBXNTE portant le document. Ajout d’une note au niveau du PRT
  destinataire</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  12.2.6.2&nbsp;: Informations du courriel MSS. Le contenu du courriel est codé
  en base 64</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  12.2.6.3.5&nbsp;: suppression de l’OBX permettant de préciser qu’un accusé
  métier de lecture MSS est attendu par le GESTIONNAIRE</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  12.3&nbsp;: suppression de la description du message ZAM^Z03^ZAM_Z01</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:36.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Annexe 2&nbsp;:
  ajout des codes erreurs 902, 903 et 904 demandés par la DNS dans la table des
  codes erreurs de traitement du message MDM</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:36.0pt;text-indent:-18.0pt"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Annexe
  3&nbsp;: modification des exemples pour prendre en compte les corrections/modifications
  de la version</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:36.0pt;text-indent:-18.0pt"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><span style="font-size:10.0pt;line-height:115%">Annexe 4&nbsp;: structure du
  message MDN-Message Disposition Notification (MSSanté)</span></p>
  </td>
 </tr>
 <tr>
  <td width="11%" colspan="3" rowspan="2" style="width:11.28%;border:solid gray 1.0pt;
  border-top:none;padding:2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" align="center" style="margin-bottom:0cm;text-align:center">1.1</p>
  </td>
  <td width="14%" colspan="2" style="width:14.78%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">ANS</p>
  </td>
  <td width="14%" colspan="2" style="width:14.82%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">Le 21/03/2024</p>
  </td>
  <td width="14%" colspan="2" style="width:14.78%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">ANS</p>
  </td>
  <td width="14%" colspan="2" style="width:14.82%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">&nbsp;</p>
  </td>
  <td width="14%" colspan="2" style="width:14.8%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">ANS</p>
  </td>
  <td width="14%" style="width:14.7%;border-top:none;border-left:none;
  border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="TBLContenu" style="margin-bottom:0cm">&nbsp;</p>
  </td>
 </tr>
 <tr>
  <td width="88%" colspan="11" style="width:88.66%;border-top:none;border-left:
  none;border-bottom:solid gray 1.0pt;border-right:solid gray 1.0pt;padding:
  2.85pt 2.85pt 2.85pt 2.85pt">
  <p class="MsoNormal">Motif et nature de la modification&nbsp;: Prise en compte
  des retours de concertation publique (04/03/2024 au 18/03/2024.</p>
  <p class="MsoListParagraphCxSpFirst" style="margin-bottom:8.0pt;text-indent:
  -18.0pt;line-height:107%"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Ajout
  du paragraphe 1.2 Ce dont ne traite pas ce volet</p>
  <p class="MsoListParagraphCxSpLast" style="margin-bottom:8.0pt;text-indent:
  -18.0pt;line-height:107%"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span>Volume
  1 – Etude fonctionnelle</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  2.1&nbsp;: correction de l’@ MSS du médecin</span></p>
  <p class="MsoListParagraphCxSpFirst" style="margin-top:0cm;margin-right:0cm;
  margin-bottom:0cm;margin-left:72.0pt;text-indent:-18.0pt;line-height:107%"><span style="line-height:107%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span>Paragraphe 2.3.1&nbsp;: cas d’usage, transmission d’une BAL
  orga vers une BAL orga&nbsp;: précisions apportées sur le point d’attention
  juste avant la figure 4. </p>
  <p class="MsoListParagraphCxSpLast" style="margin-top:0cm;margin-right:0cm;
  margin-bottom:0cm;margin-left:72.0pt;text-indent:-18.0pt;line-height:107%"><span style="line-height:107%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="line-height:107%">Section 3.2&nbsp;: les processus,
  précision apportée sur les métadonnées MSS sont limitées au masquage des
  documents aux PS et à la mise en visibilité au patient/rep légaux.</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:36.0pt;text-indent:-18.0pt"><span style="font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><span style="font-size:10.0pt;line-height:115%">Volume 2 – Etude technique</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  7&nbsp;: Modification de la rédaction du périmètre de la transaction&nbsp;:
  «&nbsp;</span>Le périmètre des spécifications s’applique à&nbsp;toute demande
  de transmission initiale/remplacement/suppression d’un document CDA-R2,
  provenant d’un courriel MSSanté réceptionné dans une BAL applicative et
  traité par la PFI de l’établissement hospitalier&nbsp;»</p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section 12.1.1&nbsp;:
  </span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Profil du
  message HL7 MDM&nbsp;: passage du segment PRT à obligatoire et répétable [1..*]</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Précision dans
  le texte sous le profil</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section 12.2.5&nbsp;:
  précisions apportées sur le peuplement des champs TXA-12 et TXA-13</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  12.2.6.1&nbsp;: OBX portant le document</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Précision (<i>Note
  2)&nbsp;:</i> il sera possible au GESTIONNAIRE ou au CONSOMMATEUR de notifier
  le PS ou le service d’une demande de traitement sur un document à condition
  que le GESTIONNAIRE ou le CONSOMMATEUR ait la capacité à maintenir une
  correspondance entre les BAL perso/orga/app et les PS/services
  correspondants.</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section 12.2.6.3.1&nbsp;:
  OBX masquage aux PS</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Dans le
  contexte de la réception d’un courriel par la PFI, la métadonnée MASQUE_PS
  devrait prendre la valeur «&nbsp;N&nbsp;» (exigence formulée dans le volet «&nbsp;Transmission
  de document(s) CDA en HL7v2&nbsp;». Dans le cas contraire, la PFI ne doit pas
  envoyer le message HL7 MDM vers le DPI.</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:72.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:&quot;Courier New&quot;">o<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Section
  12.2.7.3.3&nbsp;: message ACK du message MDM</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Ajout du champ
  ERR-5 qui permet de préciser l’erreur de traitement de la demande sur le
  document au niveau du CONSOMMATEUR</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Précisions des
  noms symboliques pour les tables HL70357 et HL70516</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:108.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:Wingdings">§<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Précisions
  apportées sur le renseignement des champs ERR-3 et ERR-5</span></p>
  <p class="TBLContenu" style="margin-top:3.0pt;margin-right:0cm;margin-bottom:
  0cm;margin-left:36.0pt;text-indent:-18.0pt"><span style="font-size:10.0pt;
  line-height:115%;font-family:Symbol">·<span style="font:7.0pt &quot;Times New Roman&quot;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  </span></span><span style="font-size:10.0pt;line-height:115%">Annexe 3&nbsp;:
  la table initiale est scindée en deux tables&nbsp;: messageErrorCondition et
  applicationErrorCondition</span></p>
  </td>
 </tr>
 <tr height="0">
  <td width="0" style="border:none"></td>
  <td width="51" style="border:none"></td>
  <td width="6" style="border:none"></td>
  <td width="50" style="border:none"></td>
  <td width="15" style="border:none"></td>
  <td width="60" style="border:none"></td>
  <td width="17" style="border:none"></td>
  <td width="43" style="border:none"></td>
  <td width="17" style="border:none"></td>
  <td width="43" style="border:none"></td>
  <td width="25" style="border:none"></td>
  <td width="34" style="border:none"></td>
  <td width="26" style="border:none"></td>
  <td width="68" style="border:none"></td>
 </tr>
</tbody></table>