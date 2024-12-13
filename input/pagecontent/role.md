<table>
  <tbody>
    <tr>
      <th>
        <p><strong>Acteur</strong></p>
      </th>
      <th>
        <p>GESTIONNAIRE</p>
      </th>
    </tr>
    <tr>
      <th>
        <p><strong>Rôle</strong></p>
      </th>
      <td>
        <p>- Le GESTIONNAIRE extrait les informations de l'archive IHE_XDM (pièce jointe du mail), analyse ces informations et construit le message HL7 MDM correspondant pour l'envoyer au CONSOMMATEUR.</p>
        <p>- Le GESTIONNAIRE réceptionne l'accusé de réception et d'intégration du message HL7 MDM, gère cet accusé et construit un accusé de lecture MSSanté (MDN-Message Disposition Notification) en fonction du statut retourné par l'acquittement du message HL7 MDM.</p>
      </td>
    </tr>
    <tr>
      <th>
        <p><strong>Acteur</strong></p>
      </th>
      <th>
        <p>CONSOMMATEUR</p>
      </th>
    </tr>
    <tr>
      <th>
        <p><strong>Rôle</strong></p>
      </th>
      <td>
        <p>- Le CONSOMMATEUR reçoit la demande du GESTIONNAIRE (transmission initiale/remplacement/suppression d'un document) sous la forme d'un message HL7 MDM, intègre si possible dans sa base de données les informations portées par le message HL7 MDM et renvoie vers le GESTIONNAIRE l'accusé de réception du message HL7 MDM.</p>
      </td>
    </tr>
  </tbody>
</table>