### Exemple Message ORU (Unsolicited Transmission of an observation message)


-   Un exemple complet de message ORU\^R01\^ORU_R01 est disponible sur
    le GitHub ANS :

-   <https://github.com/ansforge/hl7V2-exemples/tree/main/Vague%202/Trans_Doc-CDA-HL7V2/TRANSMISSION_DOCS_CDA_EN_HL7V2_V2.1/ORU>

Ci-dessous quelques exemples non exhaustifs des possibilités d'échange
et de partage

**Exemple 0 :** Transmission initiale d'un CR de biologie
validé en CDA-R2 (niveau 1 et niveau 3) pour partage et échange sans les
restrictions.

_OBX-11=F :_ La validation du document pour permettre sa
publication est portée par l'OBX-11 (Observation Resultat Status)

_Extrait Message, Segments OBX :_ Transmission du CR de
biologie avec balises spécifiées pour le DMP et MSSANTE. Une adresse
mail de réponse est indiquée ainsi qu'un corps de mail pour le
professionnel de santé. Le Créateur de document(s) demande à recevoir
les accusés métier de réception DMP/MSSanté et de lecture MSSanté.

```
OBX\|1\|ED\|11502-2\^CR d\'examens
biologiques\^LN\|\|\^TEXT\^XML\^Base64\^RG9jdW1lbnQgbcOpZGljYWwgYXUgZm
9ybWF0IENEQQ\|\|\|\|\|\|F\|

PRT\|\|UC\|\|SB\^Send
by\^participation\|801234567866\^Dupont\^Jean\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|Organisation-X\^\^\^\^\^ASIP-SANTE-ST&1.2.250.1.71.4.2.2&ISO\^FINEG\^\^\^[300017985](https://finess.sante.gouv.fr/fininter/jsp/actionDetailEntiteJuridique.do?noFiness=300017985&oldFiness=300780152)

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|101234567897\^Hoda\^Adam\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|

\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|\|\|\|\|\|12\|\|\|\|\|\^\^X.400\^appliExemple@hopitalB.mssante.fr

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^146026322000196@patient.mssante.fr

PRT\|\|UC\|\|REPLY\^Reply
to\^participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

OBX\|2\|ED\|11502-2\^CR d\'examens
biologiques\^LN\|\|\^TEXT\^XML\^Base64\^RG9jdW1lbnQgbWVkY2lhbCBhdSBmb
3JtYXQgQ0RBIG5pdmVhdSAx\|\|\|\|\|\|F\|

OBX\|3\|CE\|MASQUE_PS\^Masqué aux professionnels de
Santé\^MetaDMPMSS\|\|N\^\^ expandedYes-NoIndicator \|\|\|\|\|\|F\|

OBX\|4\|CE\|INVISIBLE_PATIENT\^Document Non Visible par le
patient\^MetaDMPMSS\|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|5\|CE\|INVISIBLE_REP_LEGAUX\^Non visible par les représentants
Légaux du
patient\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|6\|CE\|CONNEXION_SECRETE\^Connexion
Secrete\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|7\|CE\|MODIF_CONF_CODE\^Modification Confidentiality
Code\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|8\|CE\|DESTDMP\^Destinataire
DMP\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|9\|CE\|DESTMSSANTEPS\^Destinataire (Professionnel de Santé,
organisation ou BAL
applicative)\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|10\|CE\|DESTMSSANTEPAT\^Destinataire
Patient\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|11\|CE\|ACK_RECEPTION\^Accusé de
réception\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|12\|CE\|ACK_LECTURE\^Accusé de
lecture\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|13\|ED\|CORPSMAIL_PS\^Corps du mail pour un
PS\^MetaDMPMSS\|\|\^TEXT\^\^Base64\^Q2hlciBjb25mcsOocmUsI

HZvdXMgdHJvdXZlcmV6IGNpLWpvaW50IGxlIENSIGTigJlpbWFnZXJpZSBkZSBNLkR1cG9udA==\|\|\|\|\|\|F\|

```
**Exemple 1 :** Transmission initiale d'un document CR
d'imagerie médicale validé en CDA-R2 (niveau 1) pour partage et échange
avec restriction Masquage PS, le message est partagé et échangé MSSanté
Patient avec les restrictions mais non échangé en MSSanté Professionnel.
Le professionnel de santé (Janet Blanc) à l'origine du message vers le
patient ne souhaite pas recevoir de réponse du patient.

_OBX-11=F :_ La validation du document pour permettre sa
publication est portée par l'OBX-11 (Observation Resultat Status)

_Extrait Message Segment OBX :_ Transmission du CR
d'imagerie médicale avec balises pour le masquage. Les informations de
l'expéditeur sont présentes. Un texte est ajouté à l'attention du
patient.

```
OBX\|1\|ED\|18748-4\^CR d'imagerie médicale\^LN
\|\|\^TEXT\^XML\^Base64\^ RG9jdW1lbnQgbWVkY2lhbCBhdSBm

b3JtYXQgQ0RBIG5pdmVhdSAx\|\|\|\|\|\|F\|

PRT\|\|UC\|\|SB\^Send
by\^participation\|801234567866\^Dupont\^Jean\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|Organisation-X\^\^\^\^\^ASIP-SANTE-ST&1.2.250.1.71.4.2.2&ISO\^FINEG\^\^\^[300017985](https://finess.sante.gouv.fr/fininter/jsp/actionDetailEntiteJuridique.do?noFiness=300017985&oldFiness=300780152)

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^146026322000196@patient.mssante.fr

OBX\|2\|CE\|MASQUE_PS\^Masqué aux professionnels de
Santé\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|3\|CE\|INVISIBLE_PATIENT\^ Document Non Visible par le
patient\^MetaDMPMSS\|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|4\|CE\|INVISIBLE_REP_LEGAUX\^Non visible par les représentants
Légaux du
patient\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|5\|CE\|CONNEXION_SECRETE\^Connexion
Secrete\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|6\|CE\|MODIF_CONF_CODE\^Modification Confidentiality
Code\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|7\|CE\|DESTDMP\^Destinataire
DMP\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|8\|CE\|DESTMSSANTEPS\^Destinataire (Professionnel de Santé,
organisation ou BAL
applicative)\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|9\|CE\|DESTMSSANTEPAT\^Destinataire
Patient\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

NTE\|1\|\|\|FIN\|

OBX\|10\|CE\|ACK_RECEPTION\^Accusé de
réception\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|11\|CE\|ACK_LECTURE_MSS\^Accusé de
lecture\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|12\|ED\|CORPSMAIL_PATIENT\^Corps du mail pour le
patient\^MetaDMPMSS \|\|\^TEXT\^\^Base64\^Qm9uam91ciBN

LkR1cG9udCwgY2ktam9pbnQgdm90cmUgQ1IgZOKAmWltYWdlcmllLg==\|\|\|\|\|F\|

```

**Exemple 2 :** Transmission d'une demande de suppression
du document CR d'imagerie médicale déjà publié et échangé en CDA-R2
(niveau 1) sans les restrictions. Le document est dépublié sur le DMP et
la PFI doit générer un message en direction des destinataires MSSanté
désignés indiquant dans le corps du courriel que le document doit être
supprimé. La PFI construit le fichier METADATA de l'archive IHE_XDM en y
insérant une extra-metadata « action » dont la valeur est « D »
(Deleted), indiquant que le document présent dans l'archive est à
supprimer. Côté consommateur, l'id du document à supprimer est extrait
du CDA à partir de l'élément clinicalDocument@id.

_OBX-11=D :_ Suppression du document, elle sera portée par
l'OBX-11 (Observation Resultat Status)

_Extrait Message Segment OBX :_ Transmission du CR
d'imagerie médicale avec balises pour le DMP/ MSSanté :

```
OBX\|1\|ED\|18748-4\^CR d'imagerie médicale\^LN\|\|\^TEXT\^XML\^Base64\^
RG9jdW1lbnQgbWVkY2lhbCBhdSBmb3Jt

YXQgQ0RBIG5pdmVhdSAx\|\|\|\|\|\|D\|

PRT\|\|UC\|\|SB\^Send
by\^participation\|801234567866\^Dupont\^Jean\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|Organisation-X\^\^\^\^\^ASIP-SANTE-ST&1.2.250.1.71.4.2.2&ISO\^FINEG\^\^\^[300017985](https://finess.sante.gouv.fr/fininter/jsp/actionDetailEntiteJuridique.do?noFiness=300017985&oldFiness=300780152)

[PRT\|\|UC\|\|RCT\^results Copies
To\^participation\|\|\|\|Radiologie\^\^\^\^\^120456789\^UF\^\^\^3435\|\|\|\|\|\|\|\^\^X.400\^radiologie@hopitalA.mssante.fr](mailto:PRT||UC||RCT||||||||||%5e%5eX.400%5eserviceA@hopitalA.mssante.fr)

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|101234567897\^Hoda\^Adam\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

OBX\|2\|CE\|MASQUE_PS\^Masqué aux professionnels de
Santé\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|3\|CE\|INVISIBLE_PATIENT\^ Document Non Visible par le
patient\^MetaDMPMSS\|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|4\|CE\|INVISIBLE_REP_LEGAUX\^Non visible par les représentants
Légaux du patient\^MetaDMPMSS \|\|N\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|5\|CE\|CONNEXION_SECRETE\^Connexion
Secrete\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|6\|CE\|MODIF_CONF_CODE\^Modification Confidentiality
Code\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|7\|CE\|DESTDMP\^Destinataire DMP\^MetaDMPMSS\|\|Y\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|8\|CE\|DESTMSSANTEPS\^Destinataire (Professionnel de Santé,
organisation ou BAL
applicative)\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|9\|CE\|DESTMSSANTEPAT\^Destinataire
Patient\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|10\|CE\|ACK_RECEPTION\^Accusé de
réception\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|11\|CE\|ACK_LECTURE\^Accusé de
lecture\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|12\|ED\|CORPSMAIL_PS\^Corps du mail pour un PS\^MetaDMPMSS
\|\|\^TEXT\^\^Base64\^Q2hlciBjb25mcsOocmUsI

HZvdXMgdHJvdXZlcmV6IGNpLWpvaW50IGxlIENSIGTigJlpbWFnZXJpZSBkZSBNLkR1cG9udA==\|\|\|\|\|\|F\|

```

**Exemple 3 :** Remplacement d'un document déjà partagé
DMP et échangé par une nouvelle version validée en CDA-R2 pour nouveau
partage et échange sans restriction, le message est partagé sur le DMP
pour « Replace ». Le code RPLC dans
clinicalDocument/relatedDocument@typeCode dans le CDA-R2^\[9\]^ permet
de constituer l'association RPLC dans la soumission XDS pour le
remplacement^\[13\]^

La PFI doit également générer un message en direction des destinataires
MSSanté désignés indiquant dans le corps du courriel le remplacement. La
PFI construit le fichier METADATA de l'archive IHE_XDM en y insérant une
extra-metadata « action » dont la valeur est « C » (Change), indiquant
que le document présent dans l'archive vient remplacer la version de
document précédente. Côté consommateur, l'id du document à remplacer est
extrait de la relation
clinicalDocument/relatedDocument/parentDocument/id.

_OBX-11=C :_ Remplacement du document, elle sera portée par
l'OBX-11 (Observation Resultat Status)

_Extrait Message Segment OBX :_ Remplacement du CR
d'imagerie médicale (nouvelle version du document) avec balises pour le
DMP et MSSanté.

```
OBX\|1\|ED\|18748-4\^CR d'imagerie
médicale\^LN\|\|\^TEXT\^XML\^Base64\^RG9jdW1lbnQgbcOpZGljYWwgYXUgZm9y

bWF0IENEQQ\|\|\|\|\|\|C\|

PRT\|\|UC\|\|SB\^Send
by\^participation\|801234567866\^Dupont\^Jean\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|Organisation-X\^\^\^\^\^ASIP-SANTE-ST&1.2.250.1.71.4.2.2&ISO\^FINEG\^\^\^[300017985](https://finess.sante.gouv.fr/fininter/jsp/actionDetailEntiteJuridique.do?noFiness=300017985&oldFiness=300780152)

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|101234567897\^Hoda\^Adam\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

PRT\|\|UC\|\|RCT\^results Copies
To\^participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^146026322000196@patient.mssante.f

OBX\|2\|CE\|MASQUE_PS\^Masqué aux professionnels de
Santé\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|3\|CE\|INVISIBLE_PATIENT\^ Document Non Visible par le
patient\^MetaDMPMSS\|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|4\|CE\|INVISIBLE_REP_LEGAUX\^Non visible par les représentants
Légaux du patient\^MetaDMPMSS\|\|N\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|5\|CE\|CONNEXION_SECRETE\^Connexion
Secrete\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|6\|CE\|MODIF_CONF_CODE\^Modification Confidentiality
Code\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|7\|CE\|DESTDMP\^Destinataire
DMP\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|8\|CE\|DESTMSSANTEPS\^Destinataire (Professionnel de Santé,
organisation ou BAL
applicative\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|9\|CE\|DESTMSSANTEPAT\^Destinataire
Patient\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|10\|CE\|ACK_RECEPTION\^Accusé de
réception\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|11\|CE\|ACK_LECTURE_MSS\^Accusé de
lecture\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|12\|ED\|CORPSMAIL_PS\^Corps du mail pour un PS\^MetaDMPMSS
\|\|\^TEXT\^\^Base64\^Q2hlciBjb25mcsOocmUsI

HZvdXMgdHJvdXZlcmV6IGNpLWpvaW50IGxlIENSIGTigJlpbWFnZXJpZSBkZSBNLkR1cG9udA==\|\|\|\|\|\|F\|


```

**Exemple 4 :** Transmission d'un document CR d'imagerie
médicale validé en CDA-R2 pour partage et envoi par MSSanté en le
rendant visible au patient grâce à la valorisation et l'interprétation
d'une balise OBX MODIF_CONF_CODE, une balise OBX INVISIBLE_PATIENT à N
permettant de préciser que le document doit être rendu visible au
patient et permettre l'échange MSSanté.

La PFI doit générer un message en direction des destinataires MSSanté
désignés indiquant dans le corps du courriel le remplacement. La PFI
construit le fichier METADATA de l'archive IHE_XDM en y insérant une
extra-metadata « action » dont la valeur est « C » (Change), indiquant
que le document présent dans l'archive vient remplacer la version de
document précédente. Côté consommateur, l'id du document à remplacer est
extrait de la relation
clinicalDocument/relatedDocument/parentDocument/id.

_OBX-11= C :_ Remplacement du document, elle sera portée par
l'OBX-11 (Observation Resultat Status)

_Extrait Message Segment OBX :_ Modification des métadonnées
du CR d'imagerie médicale (nouvelle version du document) avec balises
spécifiées pour le DMP et MSSANTE.

```
OBX\|1\|ED\|18748-4\^CR d'imagerie
médicale\^LN\|\|\^TEXT\^XML\^Base64\^RG9jdW1lbnQgbcOpZGljYWwgYXUgZm9y

bWF0IENEQQ\|\|\|\|\|\|C\|

PRT\|\|UC\|\|SB\^Send
by\^participation\|801234567866\^Dupont\^Jean\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|Organisation-X\^\^\^\^\^ASIP-SANTE-ST&1.2.250.1.71.4.2.2&ISO\^FINEG\^\^\^[300017985](https://finess.sante.gouv.fr/fininter/jsp/actionDetailEntiteJuridique.do?noFiness=300017985&oldFiness=300780152)

PRT\|\|UC\|\|RCT\^Result Copies
To\^participation\|101234567897\^Hoda\^Adam\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|\|\|\|\|\|12\|\|\|\|\|\^\^X.400\^appliExemple@hopitalB.mssante.fr

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^146026322000196@patient.mssante.fr

PRT\|\|UC\|\|REPLY\^Reply
to\^participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

OBX\|2\|CE\|MASQUE_PS\^Masqué aux professionnels de
Santé\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|3\|CE\|INVISIBLE_PATIENT\^ Document Non Visible par le
patient\^MetaDMPMSS\|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|4\|CE\|INVISIBLE_REP_LEGAUX\^Non visible par les représentants
Légaux du
patient\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|5\|CE\|CONNEXION_SECRETE\^Connexion
Secrete\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|6\|CE\|MODIF_CONF_CODE\^Modification Confidentiality
Code\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|7\|CE\|DESTDMP\^Destinataire
DMP\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|8\|CE\|DESTMSSANTEPS\^Destinataire (Professionnel de Santé,
organisation ou BAL
applicative)\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|9\|CE\|DESTMSSANTEPAT\^Destinataire
Patient\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|10\|CE\|ACK_RECEPTION\^Accusé de
réception\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|11\|CE\|ACK_LECTURE_MSS\^Accusé de
lecture\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

```

### Message MDM (Medical Document Management)

-   Un exemple complet de message MDM\^T02\^MDM_T02 est disponible sur
    le GitHub ANS :

-   <https://github.com/ansforge/hl7V2-exemples/tree/main/Vague%202/Trans_Doc-CDA-HL7V2/TRANSMISSION_DOCS_CDA_EN_HL7V2_V2.1/MDM>

Ci-dessous quelques exemples non exhaustifs des possibilités d'échange
et de partage

**Exemple 0 :** Transmission initiale d'un document CR
d'imagerie médicale validé en CDA-R2 pour partage et échange sans les
restrictions.

_OBX-11=F :_ La validation du document pour permettre sa publication est
portée par l'OBX-11 (Observation Result Status)

_Code : T02 :_ Envoi d'un document initial

_Extrait Message Segment OBX :_ Transmission du CR
d'imagerie médicale avec balises pour le DMP et MSSANTE. Un corps de
mail pour le professionnel de santé est spécifié.

```
OBX\|1\|ED\|18748-4\^CR d'imagerie
médicale\^LN\|\|\^text\^XML\^Base64\^RG9jdW1lbnQgbcOpZGljYWwgYXUgZm9y

bWF0IENEQQ\|\|\|\|\|\|F\|

PRT\|\|UC\|\|SB\^Send
by\^participation\|801234567866\^Dupont\^Jean\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|Organisation-X\^\^\^\^\^ASIP-SANTE-ST&1.2.250.1.71.4.2.2&ISO\^FINEG\^\^\^[300017985](https://finess.sante.gouv.fr/fininter/jsp/actionDetailEntiteJuridique.do?noFiness=300017985&oldFiness=300780152)

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|101234567897\^Hoda\^Adam\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

PRT\|\|UC\|\|RCT\^results Copies
To\^participation\|\|\|\|\|\|12\|\|\|\|\|\^\^X.400\^appliExemple@hopitalB.mssante.fr

[PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|\|\|\|Radiologie\^\^\^\^\^120456789\^UF\^\^\^3435\|\|\|\|\|\|\|\^\^X.400\^radiologie@hopitalA.mssante.fr](mailto:PRT||UC||RCT||||||||||%5e%5eX.400%5eserviceA@hopitalA.mssante.fr)

PRT\|\|UC\|\|RCT\^Results Copies Toç
participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^146026322000196@patient.mssante.fr

PRT\|\|UC\|\|REPLY\^Reply
to\^participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

OBX\|2\|CWE\|MASQUE_PS\^Masqué aux professionnels de
Santé\^MetaDMPMSS\|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|3\|CWE\|INVISIBLE_PATIENT\^ Document Non Visible par le
patient\^MetaDMPMSS \|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|4\|CWE\|INVISIBLE_REP_LEGAUX\^Non visible par les représentants
Légaux du patient\^MetaDMPMSS\|\|N\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|5\|CWE\|CONNEXION_SECRETE\^Connexion Secrete\^MetaDMPMSS\|\|N\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|6\|CWE\|MODIF_CONF_CODE\^Modification Confidentiality
Code\^MetaDMPMSS \|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|7\|CWE\|DESTDMP\^Destinataire DMP\^MetaDMPMSS\|\|Y\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|8\|CWE\|DESTMSSANTEPS\^Destinataire (Professionnel de Santé,
organisation ou BAL applicative)\^MetaDMPMSS\|\|Y\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|9\|CWE\|DESTMSSANTEPAT\^Destinataire Patient\^MetaDMPMSS\|\|Y\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|10\|CWE\|ACK_RECEPTION\^Accusé de réception\^MetaDMPMSS\|\|Y\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|11\|CWE\|ACK_LECTURE_MSS\^Accusé de lecture\^MetaDMPMSS\|\|Y\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|12\|ED\|CORPSMAIL_PS\^Corps du mail pour un PS\^MetaDMPMSS
\|\|\^text\^\^Base64\^Q2hlciBjb25mcsOocmUsI

HZvdXMgdHJvdXZlcmV6IGNpLWpvaW50IGxlIENSIGTigJlpbWFnZXJpZSBkZSBNLkR1cG9udA==\|\|\|\|\|\|F\|

```

**Exemple 1 :** Transmission initiale d'un document CR
d'imagerie Médicale validé en CDA-R2 pour partage et échange avec
restriction Masquage Médecin, le message est partagé et échangé MSSanté
Patient avec les restrictions mais non échangé en MSSanté Professionnel.

_OBX-11=F :_ La validation du document pour permettre sa publication est
portée par l'OBX-11 (Observation Result Status)

_Code : T02:_ Envoi d'un document initial

_Extrait Message Segment OBX :_ Transmission du CR
d'imagerie médicale avec balises pour le masquage. Les informations de
l'expéditeur sont présentes. Un texte est ajouté à l'attention du
patient.

```
OBX\|1\|ED\|18748-4\^CR d'imagerie
médicale\^LN\|\|\^text\^XML\^Base64\^RG9jdW1lbnQgbcOpZGljYWwgYXUgZm9y

bWF0IENEQQ\|\|\|\|\|\|F\|

PRT\|\|UC\|\|SB\^send
by\^participation\|801234567866\^Dupont\^Jean\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|Organisation-X\^\^\^\^\^ASIP-SANTE-ST&1.2.250.1.71.4.2.2&ISO\^FINEG\^\^\^[300017985](https://finess.sante.gouv.fr/fininter/jsp/actionDetailEntiteJuridique.do?noFiness=300017985&oldFiness=300780152)

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^146026322000196@patient.mssante.fr

OBX\|2\|CWE\|MASQUE_PS\^Masqué aux professionnels de
Santé\^MetaDMPMSS\|\|Y\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|3\|CWE\|INVISIBLE_PATIENT\^ Document Non Visible par le
patient\^MetaDMPMSS \|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|4\|CWE\|INVISIBLE_REP_LEGAUX\^Non visible par les représentants
Légaux du patient\^MetaDMPMSS\|\|N\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|5\|CWE\|CONNEXION_SECRETE\^Connexion Secrete\^MetaDMPMSS\|\|N\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|6\|CWE\|MODIF_CONF_CODE\^Modification Confidentiality
Code\^MetaDMPMSS \|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|7\|CWE\|DESTDMP\^Destinataire DMP\^MetaDMPMSS\|\|Y\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|8\|CWE\|DESTMSSANTEPS\^Destinataire (Professionnel de Santé,
organisation ou BAL applicative) \^MetaDMPMSS\|\|N\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|9\|CWE\|DESTMSSANTEPAT\^Destinataire Patient\^MetaDMPMSS\|\|Y\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|10\|CWE\|ACK_RECEPTION\^Accusé de réception\^MetaDMPMSS\|\|Y\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|11\|CWE\|ACK_LECTURE_MSS\^Accusé de lecture\^MetaDMPMSS\|\|Y\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|12\|ED\|CORPSMAIL_PATIENT\^Corps du mail pour le
patient\^MetaDMPMSS \|\|\^text\^\^Base64\^Qm9uam91ciBN

LkR1cG9udCwgY2ktam9pbnQgdm90cmUgQ1IgZOKAmWltYWdlcmllLg==\|\|\|\|\|F\|


```

**Exemple 2 :** Transmission d'une demande de suppression
du document CR déjà publié et échangé en CDA-R2 sans les restrictions.
Le document est dépublié sur le DMP et la PFI doit générer un message en
direction des destinataires MSSanté désignés indiquant dans le corps du
courriel que le document doit être supprimé.

_OBX-11=D :_ Suppression du document, elle sera portée par l'OBX-11
(Observation Resultat Status)

_Code : T04 :_ Notification de changement du statut du
document, accompagnée du document en question.

_Extrait Message Segment OBX :_ Suppression du CR d'imagerie
avec balises pour le DMP et MSSanté

```
OBX\|1\|ED\|18748-4\^CR d'imagerie
médicale\^LN\|\|\^text\^XML\^Base64\^RG9jdW1lbnQgbcOpZGljYWwgYXUgZm9y

bWF0IENEQQ\|\|\|\|\|\|D\|

PRT\|\|UC\|\|SB\^send
by\^participation\|801234567866\^Dupont\^Jean\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|Organisation-X\^\^\^\^\^ASIP-SANTE-ST&1.2.250.1.71.4.2.2&ISO\^FINEG\^\^\^[300017985](https://finess.sante.gouv.fr/fininter/jsp/actionDetailEntiteJuridique.do?noFiness=300017985&oldFiness=300780152)
PRT\|\|UC\|\|RCT\|\|\|\|\|\|\|\|\|\|\^\^X.400\^thomas.homme@mailiz.mssante.fr

PRT\|\|UC\|\|RCT\^results Copies
To\^participation\|101234567897\^Hoda\^Adam\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

OBX\|2\|CWE\|MASQUE_PS\^Masqué aux professionnels de
Santé\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|3\|CWE\|INVISIBLE_PATIENT\^ Document Non Visible par le
patient\^MetaDMPMSS\|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|4\|CWE\|INVISIBLE_REP_LEGAUX\^Non visible par les représentants
Légaux du
patient\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|5\|CWE\|CONNEXION_SECRETE\^Connexion Secrete\^MetaDMPMSS\|\|N\^\^
expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|6\|CWE\|MODIF_CONF_CODE\^Modification Confidentiality
Code\^MetaDMPMSS \|\|N\^\^ expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|7\|CWE\|DESTDMP\^Destinataire
DMP\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|8\|CWE\|DESTMSSANTEPS\^Destinataire (Professionnel de Santé,
organisation ou BAL
applicative)\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|9\|CWE\|DESTMSSANTEPAT\^Destinataire
Patient\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|10\|CWE\|ACK_RECEPTION\^Accusé de
réception\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|11\|CWE\|ACK_LECTURE_MSS\^Accusé de
lecture\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|12\|ED\|CORPSMAIL_PS\^Corps du mail pour un PS\^MetaDMPMSS
\|\|\^text\^\^Base64\^Q2hlciBjb25mcsOocmUsI

HZvdXMgdHJvdXZlcmV6IGNpLWpvaW50IGxlIENSIGTigJlpbWFnZXJpZSBkZSBNLkR1cG9udA==\|\|\|\|\|\|F\|


```

**Exemple 3 :** Remplacement d'un document CR d'imagerie
médicale déjà partagé DMP et échangé par une nouvelle version validée en
CDA-R2 pour nouveau partage et échange sans restriction, le message est
partagé DMP pour « Replace ». Le code RPLC dans
clinicalDocument/relatedDocument@typeCode dans le CDA-R2^\[9\]^ permet
de constituer l'association RPLC dans la soumission XDS pour le
remplacement ^\[13\]^

La PFI doit également générer un message en direction des destinataires
MSSanté désignés indiquant dans le corps du courriel le remplacement. La
PFI construit le fichier METADATA de l'archive IHE_XDM en y insérant une
extra-metadata « action » dont la valeur est « C » (Change), indiquant
que le document présent dans l'archive vient remplacer la version de
document précédente. Côté consommateur, l'id du document à remplacer est
extrait de la relation
clinicalDocument/relatedDocument/parentDocument/id.

_OBX-11=C :_ Remplacement du document, elle sera portée par l'OBX-11
(Observation Resultat Status)

_Code : T10 :_ Remplacement, par une version ultérieure,
d'un document communiqué auparavant

_Extrait Message Segment OBX :_ Remplacement du CR
d'imagerie Médicale avec balises pour le DMP et MSSANTE

```
OBX\|1\|ED\|18748-4\^CR d'imagerie
médicale\^LN\|\|\^text\^XML\^Base64\^RG9jdW1lbnQgbcOpZGljYWwgYXUgZm9y

bWF0IENEQQ\|\|\|\|\|\|C\|

PRT\|\|UC\|\|SB\^Send
by\^participation\|801234567866\^Dupont\^Jean\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|Organisation-X\^\^\^\^\^ASIP-SANTE-ST&1.2.250.1.71.4.2.2&ISO\^FINEG\^\^\^[300017985](https://finess.sante.gouv.fr/fininter/jsp/actionDetailEntiteJuridique.do?noFiness=300017985&oldFiness=300780152)

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|101234567897\^Hoda\^Adam\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

PRT\|\|UC\|\|RCT\^results Copies
To\^participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^146026322000196@patient.mssante.fr

OBX\|2\|CWE\|MASQUE_PS\^Masqué aux professionnels de
Santé\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|3\|CWE\|INVISIBLE_PATIENT\^ Document Non Visible par le
patient\^MetaDMPMSS \|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|4\|CWE\|INVISIBLE_REP_LEGAUX\^Non visible par les représentants
Légaux du
patient\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|5\|CWE\|CONNEXION_SECRETE\^Connexion
Secrete\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|6\|CWE\|MODIF_CONF_CODE\^Modification Confidentiality
Code\^MetaDMPMSS \|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|7\|CWE\|DESTDMP\^Destinataire
DMP\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|8\|CWE\|DESTMSSANTEPS\^Destinataire (Professionnel de Santé,
organisation ou BAL
applicative)\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|9\|CWE\|DESTMSSANTEPAT\^Destinataire
Patient\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|10\|CWE\|ACK_RECEPTION\^Accusé de
réception\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|11\|CWE\|ACK_LECTURE_MSS\^Accusé de
lecture\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|12\|ED\|CORPSMAIL_PS\^Corps du mail pour un PS\^MetaDMPMSS
\|\|\^text\^\^Base64\^Q2hlciBjb25mcsOocmUsI

HZvdXMgdHJvdXZlcmV6IGNpLWpvaW50IGxlIENSIGTigJlpbWFnZXJpZSBkZSBNLkR1cG9udA==\|\|\|\|\|\|F\|


```

**Exemple 4 :** Transmission d'un document CR d'imagerie
médicale validé en CDA-R2 pour partage et échange en le rendant visible
au patient grâce à la valorisation et l'interprétation d'une balise OBX
MODIF_CONF_CODE, une balise OBX INVISIBLE_PATIENT à N permettant de
préciser que le document doit être rendu visible au patient et permettre
l'échange MSSanté.

La PFI doit générer un message en direction des destinataires MSSanté
désignés indiquant dans le corps du courriel le remplacement. La PFI
construit le fichier METADATA de l'archive IHE_XDM en y insérant une
extra-metadata « action » dont la valeur est « C » (Change), indiquant
que le document présent dans l'archive vient remplacer la version de
document précédente. Côté consommateur, l'id du document à remplacer est
extrait de la relation
clinicalDocument/relatedDocument/parentDocument/id.

_OBX-11=C :_ Remplacement du document, elle sera portée par l'OBX-11
(Observation Resultat Status)

_Code : T10 :_ Remplacement, par une version ultérieure,
d'un document communiqué auparavant

_Extrait Message Segment OBX :_ Transmission du CR
d'imagerie médicale avec balises spécifiées pour le DMP et MSSANTE. Une
adresse mail de réponse est précisée.

```
OBX\|1\|ED\|18748-4\^CR d'imagerie
médicale\^LN\|\|\^text\^XML\^Base64\^RG9jdW1lbnQgbcOpZGljYWwgYXUgZm9y

bWF0IENEQQ\|\|\|\|\|\|C\|

PRT\|\|UC\|\|SB\^Send
by\^participation\|801234567866\^Dupont\^Jean\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|\|Organisation-X\^\^\^\^\^ASIP-SANTE-ST&1.2.250.1.71.4.2.2&ISO\^FINEG\^\^\^[300017985](https://finess.sante.gouv.fr/fininter/jsp/actionDetailEntiteJuridique.do?noFiness=300017985&oldFiness=300780152)

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|101234567897\^Hoda\^Adam\^\^\^\^\^\^ASIP-SANTE-
PS&1.2.250.1.71.4.2.1&ISO\^D\^\^\^RPPS\|\|

\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|\|\|\|\|\|12\|\|\|\|\|\^\^X.400\^appliExemple@hopitalB.mssante.fr

PRT\|\|UC\|\|RCT\^Results Copies
To\^participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^146026322000196@patient.mssante.fr

PRT\|\|UC\|\|REPLY\^Reply
to\^participation\|\|\|\|\|\|\|\|\|\|\|\^\^X.400\^adam.hoda@medecin.mssante.fr

OBX\|2\|CWE\|MASQUE_PS\^Masqué aux professionnels de
Santé\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|3\|CWE\|INVISIBLE_PATIENT\^ Document Non Visible par le
patient\^MetaDMPMSS \|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|4\|CWE\|INVISIBLE_REP_LEGAUX\^Non visible par les représentants
Légaux du
patient\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|5\|CWE\|CONNEXION_SECRETE\^Connexion
Secrete\^MetaDMPMSS\|\|N\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|6\|CWE\|MODIF_CONF_CODE\^Modification Confidentiality
Code\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|7\|CWE\|DESTDMP\^Destinataire
DMP\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|8\|CWE\|DESTMSSANTEPS\^Destinataire (Professionnel de Santé,
organisation ou BAL
applicative)\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|9\|CWE\|DESTMSSANTEPAT\^Destinataire
Patient\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|10\|CWE\|ACK_RECEPTION\^Accusé de
réception\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|11\|CWE\|ACK_LECTURE_MSS\^Accusé de
lecture\^MetaDMPMSS\|\|Y\^\^expandedYes-NoIndicator\|\|\|\|\|\|F\|

OBX\|13\|XTN\|REPLY_TO\^Adresse mail de réponse\|\|\^\^X.400\^
adam.homme@mailiz.mssante.fr\|\|\|\|\|\|F\|
```