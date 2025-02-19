
![Logo_LEF_CI-SIS](https://user-images.githubusercontent.com/48218773/227532484-eff82649-4e42-49c6-966a-dc3ea78cf59c.png)

[![Workflow Init](https://github.com/ansforge/IG-fhir-partage-de-documents-de-sante/actions/workflows/fhir-workflows.yml/badge.svg)](https://github.com/ansforge/IG-fhir-partage-de-documents-de-sante/actions/workflows/fhir-workflows.yml)

Ce repository concerne la transformation la version pdf du volet "Transmission au LPS d'un document CDA provenant d'un courriel MSSanté" en guide d'implémentation puis les nouvelles versions de ce volet à partir de la version 1.1.1

**Le volet du CI-SIS est publié ici : [https://esante.gouv.fr/transmission-au-lps-de-documents-cda-provenant-dun-courriel-mssante](https://esante.gouv.fr/transmission-au-lps-de-documents-cda-provenant-dun-courriel-mssante)**


# Contexte

## Contexte métier du projet

Ce document présente les spécifications techniques du volet « Transmission au DPI/RIS de documents CDA provenant d'un courriel MSSanté » (ST Transmission au DPI/RIS de documents CDA provenant d'un courriel MSSanté) permettant la transmission d’un document médical au format CDA-R2 (Clinical Document Architecture Release 2) entre une Plateforme d’Intermédiation (PFI) et le logiciel du professionnel de santé (LPS : DPI ou RIS) après réception d’un courriel sur la Boîte Aux Lettres (BAL) applicative MSSanté de la PFI.


La PFI extrait les documents médicaux de l’archive du courriel MSSanté puis les transmet unitairement au LPS (DPI/RIS) par un flux HL7v2 de type MDM (Medical Document Management). Le LPS (DPI/RIS) acquitte le message HL7 MDM et transmet, le cas échéant, l’accusé de lecture des informations portées par le message MDM au niveau du LPS.
Cette spécification technique est basée sur les Spécifications Fonctionnelles des Echanges du volet « Transmission au DPI/RIS de documents CDA provenant d'un courriel MSSanté » (SFE Articulation PFI/DPI) et sur le standard HL7v2.6.


Seul le processus « Transmission de documents reçus par MSS » des spécifications fonctionnelles des échanges a été retenu dans le cadre de cette spécification technique. Le processus « Consommation de documents du DMP » n’a pas été retenu.

## Contexte technique du projet

**Transformation de la version pdf du volet "Transmission au LPS d'un document CDA provenant d'un courriel MSSanté" en guide d'implémentation.**

# CI/CD

Les workflows associés à ce repository (.github/workflows) permettent :

* D'executer Sushi pour vérifier la grammaire
* De publier les pages : https://ansforge.github.io/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/{nom de la branche}/ig/

Accès à la version ci-build : https://ansforge.github.io/IG-hl7v2-volet-trans-lps-doc-cda-courriel-mss/main/ig/

# Notes


## Acronymes
<table width="100%">
<tbody>
<tr>
<td width="22%">
<p>Sigle / Acronyme</p>
</td>
<td width="77%">
<p>Signification</p>
</td>
</tr>
<tr>
<td width="22%">
<p><strong>ACK&nbsp;:</strong></p>
</td>
<td width="77%">
<p>General acknowledge message</p>
</td>
</tr>
<tr>
<td width="22%">
<p><strong>BAL&nbsp;:</strong></p>
</td>
<td width="77%">
<p>Bo&icirc;te aux lettres</p>
</td>
</tr>
<tr>
<td width="22%">
<p><strong>CDA-R2&nbsp;:</strong></p>
</td>
<td width="77%">
<p>Clinical Document Architecture Release 2</p>
</td>
</tr>
<tr>
<td width="22%">
<p><strong>DPI&nbsp;: </strong></p>
</td>
<td width="77%">
<p>Dossier Patient Informatis&eacute;</p>
</td>
</tr>
<tr>
<td width="22%">
<p><strong>INS&nbsp;:</strong></p>
</td>
<td width="77%">
<p>Identit&eacute; Nationale de Sant&eacute;</p>
</td>
</tr>
<tr>
<td width="22%">
<p><strong>LPS&nbsp;:</strong></p>
</td>
<td width="77%">
<p>Logiciel Professionnel de Sant&eacute;</p>
</td>
</tr>
<tr>
<td width="22%">
<p><strong>MDM&nbsp;: </strong></p>
</td>
<td width="77%">
<p>M&eacute;dical Document Management</p>
</td>
</tr>
<tr>
<td width="22%">
<p><strong>MLLP&nbsp;: </strong></p>
</td>
<td width="77%">
<p>Minimal Lower Layer Protocol</p>
</td>
</tr>
<tr>
<td width="22%">
<p><strong>MSSant&eacute;&nbsp;:</strong></p>
</td>
<td width="77%">
<p>Messagerie S&eacute;curis&eacute;e de Sant&eacute;</p>
</td>
</tr>
<tr>
<td width="22%">
<p><strong>NOS&nbsp;: </strong></p>
</td>
<td width="77%">
<p>Nomenclature des Objets de Sant&eacute;</p>
</td>
</tr>
<tr>
<td width="22%">
<p><strong>PFI&nbsp;: </strong></p>
</td>
<td width="77%">
<p>Plateforme Interm&eacute;diation</p>
</td>
</tr>
</tbody>
</table>
