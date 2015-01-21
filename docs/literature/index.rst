OpenAIRE Guidelines for Literature Repositories
===============================================

{{TOCright}}
== Introduction ==
=== Aim ===
The OpenAIRE Guidelines for Literature Repository Managers 3.0 provide
orientation for repository managers to define and implement their local data
management policies according to the requirements of the OpenAIRE - Open Access
Infrastructure for Research in Europe.

Initially, the requirements of the OpenAIRE infrastructure, and the previous
versions of the OpenAIRE Guidelines, were established to support and monitor the
implementation of the `FP7 OA pilot <http://www.openaire.eu>`_. However, this
version of the Guidelines, according to the expansion of the aims of the
OpenAIRE project and infrastructure, has a broader scope. In fact, these
guidelines are intended to guide repository manager to expose to the OpenAIRE
infrastructure not only EC funded publications, but also other Open Access
publications, regardless of their funding.

So, by implementing these Guidelines, repository managers will not only be
enabling authors who deposit publications in their repository to fulfill the EC
Open Access requirements, and eventually also the requirements of other
(national or international) funders with whom OpenAIRE cooperates,
but also incorporating their publications into the OpenAIRE infrastructure for
discoverability and utilizing value-added services provided by the OpenAIRE portal.

According to the ongoing expansion and anticipating the merger of the DRIVER
Guidelines into the context of OpenAIRE Guidelines, detailed content from the
DRIVER Guidelines 2.0 was adapted and added into this version of the Guidelines.
The OpenAIRE Guidelines for Literature Repository Managers 3.0 are now only a
part of a set of OpenAIRE Guidelines that also includes the OpenAIRE Guidelines
for Data Archive Managers  and the OpenAIRE CERIF-XML profile.

=== What's new ===
In comparison with previous versions of the Guidelines, this 3.0 version introduces
three main changes:
# The OpenAIRE OAI set has been renamed from <code>ec_fundedresources</code> to <code>openaire</code>.
# New elements for indicating alternative identifiers, relations to other publications (references), and relations to research datasets have been defined.
# The recommendations on how to use the Dublin Core elements have been inherited from the DRIVER Guidelines.

== Acknowledgements & Contributors ==
=== Editors ===
* Mathias Loesch (Bielefeld University, Germany)
* Eloy Rodrigues (University of Minho, Portugal)
* Pedro Principe (University of Minho, Portugal)
* Jochen Schirrwagen (Bielefeld University, Germany)

=== Experts & Reviewers ===
* Jordan Biserkov (Pensoft, Bulgaria)
* Natasa Bulatovic (Max Planck Digital Library, Germany)
* Paolo Manghi (CNR, Italy)
* Natalia Manola (University of Athens, Greece)
* Najla Rettberg (University of Goettingen, Germany)
* Birgit Schmidt (University of Goettingen,Germany)
* Peter Stanchev (Kettering University, USA)

== Versions ==
* 1.0 July 2010
Initial document
* 1.1 November 2010
Correction of names and references; addition of license and version statement
* 2.0 October 2012
Compatibility for aggregators; extended Namespace for Project Identification
* 3.0 beta December 2012
The OpenAIRE OAI set has been renamed from <code>ec_fundedresources</code> to <code>openaire</code>.
New relation elements for indicating external identifiers, references and connections to datasets.
* 3.0 April 2013

== OpenAIRE Use of OAI-DC ==
This documentation uses the following namespace abbreviation:
* dc: http://purl.org/dc/elements/1.1/

{| class="wikitable"
|-
! OpenAIRE-Field !! OAI-DC Element !! Refinement by Vocabulary
|-
| [[Literature_Guidelines:_Metadata_Field_Title|Title]]|| dc:title || --
|-
| [[Literature_Guidelines:_Metadata_Field_Creator|Creator]] || dc:creator || --
|-
| [[Literature_Guidelines:_Metadata_Field_Project_Identifier|Project Identifier]] || dc:relation || info:eu-repo/grantAgreement/
|-
| [[Literature_Guidelines:_Metadata_Field_Access_Level|Access Level]] || dc:rights || info:eu-repo/semantics
|-
| [[Literature_Guidelines:_Metadata_Field_License|License Condition]] || dc:rights || --
|-
| [[Literature_Guidelines:_Metadata_Field_Embargo_End_Date|Embargo End]] || dc:date || info:eu-repo/date/embargoEnd
|-
| [[Literature_Guidelines:_Metadata_Field_Alternative_Identifier|Alternative Identifier]] || dc:relation || info:eu-repo/semantics/altIdentifier/
|-
| [[Literature_Guidelines:_Metadata_Field_Referenced_Publication|Publication Reference]] || dc:relation || info:eu-repo/semantics/reference
|-
| [[Literature_Guidelines:_Metadata_Field_Referenced_Dataset|Dataset Reference]] || dc:relation || info:eu-repo/semantics/dataset/
|-
| [[Literature_Guidelines:_Metadata_Field_Subject|Subject]] || dc:subject || --
|-
| [[Literature_Guidelines:_Metadata_Field_Description|Description]] || dc:description || --
|-
| [[Literature_Guidelines:_Metadata_Field_Publisher|Publisher]] || dc:publisher || --
|-
| [[Literature_Guidelines:_Metadata_Field_Contributor|Contributor]] || dc:contributor || --
|-
| [[Literature_Guidelines:_Metadata_Field_Date_of_Publication|Publication Date]] || dc:date || --
|-
| [[Literature_Guidelines:_Metadata_Field_Publication_Type|Publication Type]] || dc:type || info:eu-repo/semantics/
|-
| [[Literature_Guidelines:_Metadata_Field_Publication_Version|Publication Version]] || dc:type || info:eu-repo/semantics/
|-
| [[Literature_Guidelines:_Metadata_Field_Format|Format]] || dc:format || --
|-
| [[Literature_Guidelines:_Metadata_Field_Resource_Identifier|Resource Identifier]] || dc:identifier || --
|-
| [[Literature_Guidelines:_Metadata_Field_Source|Source]] || dc:source || --
|-
| [[Literature_Guidelines:_Metadata_Field_Language|Language]] || dc:language || --
|-
| [[Literature_Guidelines:_Metadata_Field_Relation|Relation]] || dc:relation || --
|-
| [[Literature_Guidelines:_Metadata_Field_Coverage|Coverage]] || dc:coverage || --
|-
| [[Literature_Guidelines:_Metadata_Field_Audience|Audience]] || dc:audience || --
|}
