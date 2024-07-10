-   *HL7 v2.6 : Chapitre 9,* message MDM (Medical Document Management) ^(1)^~,~

-   [Extension française du profil IHE PAM : PAM.fr, version 2.11](https://old.interopsante.org/offres/doc_inline_src/412/Publication-IHE_FRANCE_PAM_National_Extension_v2.11.pdf)

-   Les types de données utilisés ^(2)^ doivent se conformer aux spécifications [« Contraintes sur les types de données HL7 v2.5 applicables aux profils d'intégration du cadre technique IT Infrastructure dans le périmètre d'IHE France » release 1.8](https://old.interopsante.org/offres/doc_inline_src/412/IHE_France_Constraints_on_HL7_data_types_for_ITI_V1.8.pdf)

-   Le choix du protocole de transport est libre. L'utilisation du protocole MLLP est à privilégier pour gérer au mieux les accusés de réception techniques (ACK).

-   Dans le cadre de cette spécification, les documents médicaux véhiculés correspondent à des documents au format CDA-R2 conformes au [volet du CI-SIS « Structuration minimale des documents de santé »](https://esante.gouv.fr/sites/default/files/media_entity/documents/ci-sis_contenu_volet-structuration-minimale_v1.15.pdf).

-   Les documents transmis par le message HL7 doivent être validés par le professionnel de santé dans l'application métier qui les a générés via un statut de validation géré en interne.

-   Les échanges MSSanté doivent prendre en compte les restrictions positionnées sur le message. (Exemple : Un document avec un masquage Médecin ne doit pas être envoyé sur le mail MSSanté du médecin).

<blockquote class="stu-note">
    <p>
    <b>(1) :</b> Les messages décrits au niveau de cette transaction implémentent la version 2.6 (message MDM) du standard HL7 mais pré adoptent le segment PRT de la version 2.9, permettant de spécifier l’expéditeur et le(s) destinataire(s) d’un courriel.
    Le message MDM permet de transmettre un seul document.
    </p>
</blockquote>

<blockquote class="stu-note">
    <p>
    <b>(2) :</b> Pour l'ensemble des champs de type CE en HL7v2.5 et CWE en HL7v2.6, la contrainte imposée en version 2.7 sur le type de donnée CE/CWE est pré adoptée. En conséquence, ces spécifications imposent de préciser le système de codage (CE/CWE.3) lorsque le code (CE/CWE.1) est renseigné. 
Les bonnes pratiques consistent à renseigner systématiquement les 3 composantes : le code, le libellé du code et le libellé de la nomenclature.
    </p>
</blockquote>