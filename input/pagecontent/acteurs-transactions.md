### Liste des Acteurs et systèmes concernés

Le présent volet met en œuvre les Acteurs IHE suivants, représentant le rôle joué par un ou plusieurs composants du système d’information :

<table>
  <tbody>
    <tr>
      <th>
        <p>Acteur</p>
      </th>
      <th>
        <p>Description</p>
      </th>
    </tr>
    <tr>
      <td>
        <p>GESTIONNAIRE</p>
      </td>
      <td>
        <p>Le GESTIONNAIRE réceptionne et transmet au système CONSOMMATEUR les demandes de transmission initiale/remplacement/suppression de document(s) provenant d'un courriel.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>CONSOMMATEUR</p>
      </td>
      <td>
        <p>Le CONSOMMATEUR réceptionne et gère les demandes de transmission initiale/remplacement/suppression de document(s) issues d'un courriel, provenant du système GESTIONNAIRE et renvoie l'accusé de traitement de la demande vers le GESTIONNAIRE.</p>
      </td>
    </tr>
  </tbody>
</table>

Le tableau suivant liste, pour chacun des acteurs, les systèmes du SIH concernés :

<table>
  <tbody>
    <tr>
      <th>
        <p>Acteur</p>
      </th>
      <th>
        <p>Systèmes concernés</p>
      </th>
    </tr>
    <tr>
      <td>
        <p>GESTIONNAIRE</p>
      </td>
      <td>
        <p>-        Les Plateformes d'Intermédiation (PFI) qui assurent la transmission de document(s) cliniques provenant d'un courriel MSSanté vers un CONSOMMATEUR (le LPS destinataire).</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>CONSOMMATEUR</p>
      </td>
      <td>
        <p>-          Tout logiciel métier (LPS) du SIH qui récupère et gère la demande de traitement du document transmis par le GESTIONNAIRE.</p>
        <p>-          Dans le contexte du SEGUR vague 2, les applications consommatrices de ces documents sont limitées au dossier patient informatisé (DPI) et au système de gestion de radiologie (RIS).</p>
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
      <th>
        <p>Acteur</p>
      </th>
      <th>
        <p>Transaction</p>
      </th>
      <th>
        <p><strong>Caractère requis/optionnel</strong></p>
      </th>
    </tr>
    <tr>
      <td>
        <p>GESTIONNAIRE</p>
      </td>
      <td>
        <p>Flux6 HL7-MDM en émission : Demande de transmission/remplacement/suppression d'un document CDA</p>
      </td>
      <td>
        <p>R</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>CONSOMMATEUR</p>
      </td>
      <td>
        <p>Flux6 HL7-MDM en réception : Demande de transmission/remplacement/suppression d'un document CDA</p>
      </td>
      <td>
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
      <th>
        <p>Acteur de ce volet</p>
      </th>
      <th>
        <p>Groupé avec un autre acteur</p>
      </th>
      <th>
        <p>Référence</p>
      </th>
    </tr>
    <tr>
      <td>
        <p>GESTIONNAIRE</p>
      </td>
      <td>
        <p>Système cible (Portable Media Importer) XDM</p>
      </td>
      <td>
        <p><a href="https://esante.gouv.fr/volet-echange-de-documents-de-sante">Volet Echange de documents de santé</a></p>
      </td>
    </tr>
    <tr>
      <td>
        <p>CONSOMMATEUR</p>
      </td>
      <td>
        <p>Content Consumer (<a href="https://www.ihe.net/uploadedFiles/Documents/PCC/IHE_PCC_TF_Vol1.pdf">TF PCC</a>)</p>
      </td>
      <td>
        <p>TF Patient Care Coordination - Appendix A: Actors definition</p>
      </td>
    </tr>
  </tbody>
</table>
<p>&nbsp;</p>

L'acteur GESTIONNAIRE est groupé avec :

-   L'acteur Système cible du [volet d'Echange de documents de santé](https://esante.gouv.fr/volet-echange-de-documents-de-sante), pour permettre à la PFI de réceptionner l'archive IHE_XDM inclue dans le courriel reçu de l'extérieur,

L'acteur CONSOMMATEUR est groupé avec :

-   L'acteur Content Consumer définit dans le [Technical Framework PCC d'IHE](https://www.ihe.net/uploadedFiles/Documents/PCC/IHE_PCC_TF_Vol1.pdf), permettant au CONSOMMATEUR de visualiser et d'importer tout ou parties du document CDA.
