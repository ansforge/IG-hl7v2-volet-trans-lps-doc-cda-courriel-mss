#### Processus collaboratif « Demande de transmission initiale de document(s) »

<div class="figure" style='text-align: center;'>
    <img src="image15.png" alt="Figure 9" title="Figure 9 : Processus collaboratif « Demande de transmission initiale de document(s) » pour intégration au niveau du CONSOMMATEUR " style="width:60%;">
    <figcaption><b>Figure 9 : Processus collaboratif « Demande de transmission initiale de document(s) » pour intégration au niveau du CONSOMMATEUR</b></figcaption>
</div>    
<br>

<table>
  <tbody>
    <tr>
      <th>
        <p>Service Attendu</p>
      </th>
      <td>
        <p>Le GESTIONNAIRE transmet au CONSOMMATEUR la demande d'intégration de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Pré-Conditions</p>
      </th>
      <td>
        <p>- Le patient est connu du CONSOMMATEUR.</p>
        <p>- Le GESTIONNAIRE détecte qu'un courriel a été reçu sur la BAL avec en pièce jointe une archive XDM.</p>
        <p>- Le GESTIONNAIRE dézippe l'archive XDM. Il vérifie qu'elle contient des documents de santé d'un patient au format CDA ainsi qu'un fichier de métadonnées.</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Post-Conditions</p>
      </th>
      <td>
        <p>Le GESTIONNAIRE trace les transmissions de document(s)</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Contraintes fonctionnelles</p>
      </th>
      <td>
        <p>La BAL du GESTIONNAIRE doit être en capacité de détecter les courriels entrants avec demande de traitement sur le(s) document(s)</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Scénario Nominal</p>
      </th>
      <td>
        <p>- Suite à la réception d'un courriel sur la BAL destinatrice, le GESTIONNAIRE transmet le document de santé de la pièce jointe au CONSOMMATEUR.</p>
        <p>- Le CONSOMMATEUR traite la demande d'intégration du document.</p>
        <p>- Le CONSOMMATEUR retourne au GESTIONNAIRE un accusé de réception de la demande d'intégration du document.</p>
      </td>
    </tr>
  </tbody>
</table>

#### Processus collaboratif « Demande de remplacement de document(s) »

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
      <th>
        <p>Service Attendu</p>
      </th>
      <td>
        <p>Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de remplacement de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Pré-Conditions</p>
      </th>
      <td>
        <p>- Le patient est connu du CONSOMMATEUR.</p>
        <p>- Le document doit être validé et identifié comme remplaçant un document précédemment envoyé par MSSanté.</p>
        <p>- Le CONSOMMATEUR dispose de la dernière version du document original dans sa base de données.</p>
        <p>- Le GESTIONNAIRE détecte qu'un courriel a été reçu sur la BAL avec en pièce jointe une archive IHE_XDM.</p>
        <p>- Le GESTIONNAIRE dézippe l'archive XDM. Il vérifie qu'elle contient des documents de santé d'un patient au format CDA ainsi qu'un fichier de métadonnées et prend connaissance du traitement à effectuer sur le(s) document(s)</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Post-Conditions</p>
      </th>
      <td>
        <p>Le GESTIONNAIRE trace les transmissions de document(s)</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Contraintes fonctionnelles</p>
      </th>
      <td>
        <p>La BAL du GESTIONNAIRE doit être en capacité de détecter les courriels entrants avec demande de traitement sur le(s) document(s)</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Scénario Nominal</p>
      </th>
      <td>
        <p>- Suite à la réception du courriel sur la BAL destinatrice, le GESTIONNAIRE transmet la demande de remplacement de documents de santé de la pièce jointe au CONSOMMATEUR</p>
        <p>- Le CONSOMMATEUR traite la demande de remplacement du document.</p>
        <p>- Le CONSOMMATEUR retourne au GESTIONNAIRE un accusé de réception de la demande de remplacement du document.</p>
        <p> </p>
      </td>
    </tr>
  </tbody>
</table>

#### Processus collaboratif « Demande de suppression de document(s) »

<div class="figure" style='text-align: center;'>
    <img src="image17.png" alt="Figure 11" title="Figure 11 : Processus collaboratif « Demande de suppression de document(s) » au niveau du CONSOMMATEUR" style="width:60%;">
    <figcaption><b>Figure 11 : Processus collaboratif « Demande de suppression de document(s) » au niveau du CONSOMMATEUR</b></figcaption>
</div>    
<br>

<table>
  <tbody>
    <tr>
      <th>
        <p>Service Attendu</p>
      </th>
      <td>
        <p>Le GESTIONNAIRE transmet au CONSOMMATEUR la demande de suppression de(s) document(s) de santé d'un patient reçue sur la BAL MSSanté destinatrice.</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Pré-Conditions</p>
      </th>
      <td>
        <p>- Le patient est connu du consommateur.</p>
        <p>- Le document doit être validé et doit correspondre à la dernière version du document envoyé au CONSOMMATEUR.</p>
        <p>- Le CONSOMMATEUR dispose de la dernière version du document original dans sa base de données.</p>
        <p>- Le GESTIONNAIRE détecte qu'un courriel a été reçu sur la BAL avec en pièce jointe une archive IHE_XDM.</p>
        <p>- Le GESTIONNAIRE dézippe l'archive XDM. Il vérifie qu'elle contient des documents de santé d'un patient au format CDA ainsi qu'un fichier de métadonnées et prend connaissance du traitement à effectuer sur le document</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Post-Conditions</p>
      </th>
      <td>
        <p>Le GESTIONNAIRE trace les transmissions de document(s)</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Contraintes fonctionnelles</p>
      </th>
      <td>
        <p>La BAL du GESTIONNAIRE doit être en capacité de détecter les courriels entrants avec demande de traitement sur le(s) document(s)</p>
      </td>
    </tr>
    <tr>
      <th>
        <p>Scénario Nominal</p>
      </th>
      <td>
        <p>- Suite à la réception d'un courriel sur la BAL destinatrice, le GESTIONNAIRE transmet la demande de suppression du document de santé de la pièce jointe au CONSOMMATEUR</p>
        <p>- Le CONSOMMATEUR traite la demande de suppression du document.</p>
        <p>- Le CONSOMMATEUR retourne au GESTIONNAIRE un accusé de réception de suppression du document.</p>
      </td>
    </tr>
  </tbody>
</table>