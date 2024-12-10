Après réception d’un courriel détecté dans une BAL applicative MSSanté, la PFI ouvre l’archive IHE_XDM contenant des documents médicaux et les transmets individuellement au LPS consommateur en utilisant un message HL7v2.6 de type MDM.

Ensuite, le LPS accuse réception de cette demande de traitement sur le document avec un message HL7v2.6 de type ACK.

<table>
  <tbody>
    <tr>
      <th>
        <p>Flux métiers</p>
      </th>
      <th>
        <p>Type de message HL7v2.6</p>
      </th>
    </tr>
    <tr>
      <td rowspan="3">
        <p>TransmissionDocuments</p>
      </td>
      <td>
        <p>Transmission initiale d'un document : L'évènement utilisé sera le T02 « Original document notification »</p>
        <p>-&gt;  <code>MDM^T02^MDM_T02</code></p>
        <p>-&gt;  OBX-11 = F (Final results; Can only be changed with a corrected result.) [HL7 Tables 0085]</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>Suppression d'un document : L'évènement utilisé sera le T04 « Document status change notification and content »</p>
        <p>-&gt;  <code>MDM^T04^MDM_T02</code></p>
        <p>-&gt;  OBX-11 = D (Deletes the OBX record) [HL7 Tables 0085]</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>Remplacement d'un document : L'évènement utilisé sera le T10 « Document replacement notification and content »</p>
        <p>-&gt;  <code>MDM^T10^MDM_T02</code></p>
        <p>-&gt;  OBX-11 = C (Record coming over is a correction and thus replaces a final result) [HL7 Tables 0085]</p>
      </td>
    </tr>
    <tr>
      <td>
        <p>ReponseTransmissionDocuments</p>
      </td>
      <td>
        <p>ACK : Acquittement du message HL7 MDM</p>
      </td>
    </tr>
  </tbody>
</table>