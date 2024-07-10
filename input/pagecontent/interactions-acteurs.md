<div class="figure">
    <img src="image19.png" alt="Figure 13" title="Figure 13 : Diagramme de séquence – Message MDM" style="width:100%;">
    <figcaption>Figure 13 : Diagramme de séquence – Message MDM</figcaption>
</div>    
<br>
La gestion de cet accusé de lecture MSSanté (MDN-Message Disposition Notification) va dépendre de l’organisation choisie par l’établissement pour traiter les courriels réceptionnés.
Ce flux d’accusé de lecture MSSanté (message MDN) rend compte de la lecture du courriel par le destinataire lorsque ce courriel est traité de façon manuelle. Dans le cas d’un traitement automatique du courriel par la PFI de l’établissement destinataire, ce flux d’accusé de lecture rend compte de la réalisation de la demande de traitement sur le document contenu dans le courriel par le logiciel métier associé à la BAL destinatrice du courriel
Dans le cas où le courriel entrant, réceptionné par une BAL organisationnelle, est transféré vers la BAL applicative associée pour traitement automatique de la demande, le message MDN généré par le GESTIONNAIRE (PFI) et envoyé à la BAL organisationnelle demandeuse est indispensable pour avertir l’utilisateur du succès ou de l’échec de la demande de traitement par le CONSOMMATEUR.
La structure du message MDN (Message Disposition Notification) est précisée [ici](struct-msg-mdn.html).
