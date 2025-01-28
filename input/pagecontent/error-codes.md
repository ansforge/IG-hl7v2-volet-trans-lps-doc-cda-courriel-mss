La table HL7 messageErrorCondition est utilisée par l’acteur CONSOMMATEUR (DPI/RIS…) en cas d’erreur technique du message HL7 MDM.

La nature de l’erreur est renseignée dans le champ ERR-3 de la structure du message ACK renvoyé par le CONSOMMATEUR au niveau du GESTIONNAIRE (PFI).
<table>
  <tbody>
    <tr>
      <th>
        <p>Code</p>
      </th>
      <th>
        <p>Libellé</p>
      </th>
      <th>
        <p>Description</p>
      </th>
    </tr>
    <tr>
      <td>
        <p>0</p>
      </td>
      <td>
        <p>Message accepted</p>
      </td>
      <td>
        <p>Message accepté</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>100</p>
      </td>
      <td>
        <p>Segment sequence error</p>
      </td>
      <td>
        <p>Les segments ne sont pas dans le bon ordre ou il manque un ou plusieurs segments requis</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>101</p>
      </td>
      <td>
        <p>Required field missing</p>
      </td>
      <td>
        <p>Un champ requis dans un segment est manquant</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>102</p>
      </td>
      <td>
        <p>Data type error</p>
      </td>
      <td>
        <p>Erreur sur un type de donnée</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>103</p>
      </td>
      <td>
        <p>Table value not found</p>
      </td>
      <td>
        <p>Table non trouvée</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>198</p>
      </td>
      <td>
        <p>Non-conformant cardinality</p>
      </td>
      <td>
        <p>Erreur de cardinalité sur un champ du message</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>199</p>
      </td>
      <td>
        <p>Other HL7 Error</p>
      </td>
      <td>
        <p>Autre type d'erreur concernant la syntaxe du message HL7</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>200</p>
      </td>
      <td>
        <p>Unsupported message type</p>
      </td>
      <td>
        <p>Type de message non supporté</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>201</p>
      </td>
      <td>
        <p>Unsupported event code</p>
      </td>
      <td>
        <p>Code évènement non supporté</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>202</p>
      </td>
      <td>
        <p>Unsupported processing</p>
      </td>
      <td>
        <p>Code process non supporté</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>203</p>
      </td>
      <td>
        <p>Unsupported version</p>
      </td>
      <td>
        <p>Version HL7 non supportée</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>207</p>
      </td>
      <td>
        <p>Application error</p>
      </td>
      <td>
        <p>Erreur de niveau applicatif dont le contenu est détaillé dans le champ ERR-5</p>
      </td>
    </tr>
  </tbody>
</table>
La table user-defined applicationErrorCondition est utilisée par l’acteur CONSOMMATEUR (DPI/RIS…) en cas d’erreur d’intégration/de remplacement ou de suppression du document CDA au niveau du CONSOMMATEUR. La nature de l’erreur applicative est renseignée dans le champ ERR-5 de la structure du message ACK renvoyé par le CONSOMMATEUR au niveau du GESTIONNAIRE.

Cette table est décrite à titre indicatif et pourra être enrichie si besoin, en fonction des retours d’implémentation.
<table>
  <tbody>
    <tr>
      <th>
        <p>Code</p>
      </th>
      <th>
        <p>Libellé</p>
      </th>
      <th>
        <p>Description</p>
      </th>
    </tr>
    <tr>
      <td>
        <p>900</p>
      </td>
      <td>
        <p>Version du document incorrecte lors d'une demande de remplacement/suppression</p>
      </td>
      <td>
        <p>Lors d'une demande de remplacement ou suppression d'un document, la version de document transmise dans le message HL7 ne correspond pas à la version la plus récente du document existant au niveau de l'application réceptrice (consommateur)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>901</p>
      </td>
      <td>
        <p>Auteur non autorisé à remplacer ou supprimer un document</p>
      </td>
      <td>
        <p>Lors d'une demande de remplacement ou suppression d'un document, l'acteur qui demande le traitement sur le document doit être l'auteur du document ou un acteur qui appartient à la même organisation que l'auteur du document original. Dans le cas contraire, le message est rejeté.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>902</p>
      </td>
      <td>
        <p>Identifiant patient inconnu</p>
      </td>
      <td>
        <p>Le patient pour lequel le traitement sur le document est demandé est inconnu de l'application réceptrice (consommateur)</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>903</p>
      </td>
      <td>
        <p>INS non présent dans le document</p>
      </td>
      <td>
        <p>Le document CDA contenu dans le message contient une liste d'identifiants de patient mais pas l'INS. Dans ce cas, la demande de traitement sur le document (intégration/remplacement/suppression) ne peut pas être réalisée de façon automatique par le système consommateur.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>904</p>
      </td>
      <td>
        <p>L'INS transmis ne correspond pas exactement à celui stocké dans la base du consommateur</p>
      </td>
      <td>
        <p>L'INS du patient est présent dans le document CDA contenu dans le message HL7 mais les traits ou le matricule ne correspondent pas exactement à ceux stockés dans le système consommateur. Dans ce cas, la demande de traitement sur le document (intégration/remplacement/suppression) ne peut pas être réalisée de façon automatique par le système consommateur.</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>905</p>
      </td>
      <td>
        <p>L'INS transmis n'est pas complet</p>
      </td>
      <td>
        <p>L'INS du patient est présent dans le document CDA contenu dans le message HL7, mais l'ensemble des traits complémentaires ne sont pas présents. Dans ce cas, la demande de traitement sur le document (intégration/remplacement/suppression) ne peut pas être réalisée de façon automatique par le système consommateur.</p>
      </td>
    </tr>
   <tr>
      <td>
        <p>906</p>
      </td>
      <td>
        <p>Erreur 'Autre'</p>
      </td>
      <td>
        <p>Si les autres codes erreurs ne correspondent pas au cas d'erreur rencontré ce code erreur peut être utilisé.</p>
      </td>
    </tr>
  </tbody>
</table>