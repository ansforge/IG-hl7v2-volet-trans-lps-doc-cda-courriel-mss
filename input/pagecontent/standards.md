
-   *HL7 v2.5 Chapitre 7*, message ORU (Unsolicited transmission of an
    observation message), *HL7 v2.6 Chapitre 9,* message MDM (Medical
    Document Management) (1)

-   Le présent document spécifie également une nouvelle structure de
    message HL7, le message ZAM spécifique à ce volet, basé sur HL7v2.6
    et utilisé pour implémenter les accusés métier (accusé de réception
    DMP, accusé de réception MSSanté et accusé de lecture MSSanté),

-   Extension française du profil IHE PAM : PAM.fr, version 2.11 (1),

-   Les types de données utilisés (2) doivent se conformer aux
    spécifications « INTEROP’SANTE : ITI - Contraintes sur les types de données HL7 v2.5 applicables aux profils d’intégration du cadre technique IT Infrastructure dans le périmètre d’IHE France - Release 1.8 – Final Text – 31 janvier 2024 »

-   Le choix du protocole de transport est libre. L'utilisation du
    protocole MLLP est à privilégier pour gérer au mieux les accusés de
    réception techniques (ACK).

-   Dans le cadre de cette spécification, les documents médicaux
    véhiculés correspondent à des documents au format CDA-R2 conformes
    au volet du CI-SIS « [Structuration minimale des documents de santé](https://esante.gouv.fr/sites/default/files/media_entity/documents/ci-sis_contenu_volet-structuration-minimale_v1.15.pdf) ».

-   Les documents transmis par le message HL7 doivent être validés par
    le professionnel de santé dans l'application métier qui les a
    générés via un statut de validation géré en interne.

-   Dans le cas d'une publication de(s) document(s) sur le DMP, l'INS du
    patient doit être qualifié en suivant [les spécifications de l'annexe
    INS CI-SIS](https://esante.gouv.fr/sites/default/files/media_entity/documents/ans_cisis-tec_annexe-ins_1.5.pdf) et les règles du corpus documentaire INS (lien?).

-   Les échanges MSSanté doivent prendre en compte les restrictions
    positionnées sur le message. (Exemple : un document avec un masquage
    Médecin ne doit pas être envoyé sur le mail MSSanté du médecin).


<blockquote class="stu-note">
    <p>
    <b>(1) :</b> Les messages décrits au niveau de cette transaction implémentent la version 2.5 (message ORU) ou la version 2.6 (message MDM) du standard HL7 mais pré adoptent le segment PRT de la version 2.9, permettant de spécifier l'expéditeur et le(s) destinataire(s) d'un courriel.
    Le message ORU permet de transmettre, si nécessaire, deux formats de
    document (CDAr2 Niv1 et CDAr2 Niv3). Le message MDM permet de transmettre un seul document.
    </p>
</blockquote>

<blockquote class="stu-note">
    <p>
    <b>(2) :</b> Pour l\'ensemble des champs de type CE en HL7v2.5 et CWE en HL7v2.6, la contrainte imposée en version 2.7 sur le type de donnée CE/CWE est pré adoptée. En conséquence, ces spécifications imposent de préciser le système de codage (CE/CWE.3) lorsque le code (CE/CWE.1) est renseigné.
    Les bonnes pratiques consistent à renseigner systématiquement les 3
    composantes : le code, le libellé du code et le libellé de la
    nomenclature.
    </p>
</blockquote>