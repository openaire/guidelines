{{TOCright}}

'''This page is the draft version of the OpenAIRE Guidelines for CRIS Managers based on CERIF-XML'''
* Released March 2014 for public review
* Deadline for comments is the 28th March 2014
* For more information we refer to the press release by OpenAIRE on 28th February: https://www.openaire.eu/news-events/public-review-of-the-openaire-guidelines-for-cris-managers-based-on-cerif-xml



== Introduction ==
=== Aim ===
OpenAIRE gathers together research output related to European funding streams, with the aim of supporting open science and tracking research impact. This content consists of open access publications and related contextual information such as datasets, supplementary material, and research/project information.

Two other sets of OpenAIRE guidelines exist for repository managers:
* OpenAIRE Guidelines for Literature Repositories 3.0
* OpenAIRE Guidelines for Data Archives 1.0

The Guidelines provide orientation for CRIS managers to expose their metadata in a way that is compatible with the OpenAIRE infrastructure. By implementing the Guidelines, CRIS managers support the inclusion and therefore the reuse of metadata in their systems within the OpenAIRE infrastructure. For developers of CRIS platforms, the Guidelines provide guidance to add supportive functionalities for CRIS managers and users. Exchange of information between individual CRIS systems and the OpenAIRE infrastructure is an example of point-to-point data exchange between CRIS systems, since the OpenAIRE infrastructure is itself a CRIS system.

=== CERIF-CRIS ===
CERIF (Common European Research Information Format) is a standard data model for research information and a recommendation by the European Union to Member States. The care and custody of CERIF was handed over by the European Union to euroCRIS [http://www.eurocris.org], a non-for-profit organisation dedicated to the interoperability of Research Information Systems (CRISs). In addition to a domain model and a formal relational (ERM) data model, CERIF defines a XML format for data exchange.
The OpenAIRE data model is CERIF-compliant and CERIF XML has been adopted by OpenAIRE as the basis for harvesting and importing metadata from CRIS systems.

We would like to thank euroCRIS for their kind support and help making these OpenAIRE Guidelines for CRIS Managers possible.

== Acknowledgements & Contributors ==

We wish to acknowledge the following contributors and also those who provided feedback outside the formal editing and reviewing work.


===Editors===

* Nikos Houssos, National Documentation Centre (EKT)/NHRF, Greece
* Brigitte Jörg, euroCRIS, the Netherlands; JeiBee Ltd., United Kingdom
* Jan Dvorak, Charles University in Prague, Czech Republic


===Experts & Reviewers===

An earlier version of these guidelines was kindly reviewed by:

* Paolo Manghi, ISTI-CNR, Italy
* Mikael K. Elbæk, Technical University of Denmark, Denmark
* Keith Jeffery, Keith G Jeffery Consultants, United Kingdom
* Anne Asserson, University of Bergen, Norway
* Teemu Kemppainen, CSC - IT Centre for Science, Finland
* Thomas Vestdam, Elsevier, Denmark
* Thorsten Höllrigl, Thomson Reuters, Germany

== Versions ==
* 0.95 Febrary 2014
Initial document

== CRIS information elements relevant for OpenAIRE  ==
CERIF is a comprehensive domain model that allows for the formal description of many aspects (contexts) inherent in the Research domain, some of them not present in the OpenAIRE information space, which currently does not aim to represent the full range of information in CERIF. The Guidelines therefore focus on those information elements in a CRIS system that are considered relevant and can be utilised within the current scope and data model of the OpenAIRE infrastructure. The interoperability use case supported by the Guidelines is the harvesting of data from individual CRIS systems by the OpenAIRE infrastructure. The data harvested should be in CERIF XML and in particular comply with a specialisation of the CERIF XML Schema that defines an OpenAIRE-specific CERIF subset. This is an example of a point-to-point exchange of CRIS information in CERIF XML for a particular application domain. The specialised OpenAIRE CERIF XML Schema is designed so that every XML file that is valid according to it is also valid according to the standard CERIF XML Schema 1.6.

[[File:DataModel_CERIF-OpenAIRE.png|200px|thumb|center|Relevant CERIF elements in the current context of OpenAIRE|]]

The Guidelines describe the subset of the CERIF data model and the relevant specialisations that constitute the set of elements for harvesting from CRIS systems through OpenAIRE. The OpenAIRE-specific elements indicated in Figure 1 discern the identified objects (e.g. person), their attributes (e.g. gender) and some compounding sets of functional vocabularies (e.g. “Author” applicable in a person-publication relationship) for setting the boundaries. The formal model is defined as an OpenAIRE-specific CERIF XML Schema specification, which is provided separately from the present document.

The following tables define the CERIF data elements to be utilised for the exchange of data between individual CRIS systems and the OpenAIRE infrastructure. The exclusive use of the defined data elements and vocabularies is mandatory, i.e. no other data elements and vocabularies can be used in the CERIF XML data exposed by CRIS systems to the OpenAIRE infrastructure. The vocabularies as currently applied or listed in the below guideline tables are mostly based on the CERIF 1.5 Semantics. Extensions are possible and will be reflected in a release after the review.

===The CERIF XML Publication Entity in the OpenAIRE context===

{| class="wikitable"
|-
! Publication (cfResPubl)
|-
|The CERIF entity cfResPubl is used in the context of OpenAIRE to represent research results that are considered text publications. Metadata about scientific journals are also represented using the cfResPubl entity.
|-
|}

{| class="wikitable"
|-
! Attributes !! Applicable Vocabularies !! Multiplicity
|-
| Internal Identifier ''cfResPubl.ResPublId'' || || 1
|-
| Publication Date ''cfResPubl.ResPublDate'' ||  || 0..1
|-
| Federated Identifiers ''cfResPubl.cfFedId.cfFedId'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
- '''DOI''' <br/>
- '''Handle''' <br/>
- '''PMCID''' <br/>
- '''ISI-Number''' <br/>
- '''SCP-Number''' <br/>
- '''ISSN''' <br/>
- '''ISBN''' <br/>
as defined in CERIF Semantics 1.5 “Identifier Types” scheme.
|| 0..N
|-
| Title ''cfResPubl.cfTitle'' ||  || 1
|-
| Subtitle ''cfResPubl.cfSubTitle'' ||  || 0..1
|-
| Description ''cfResPubl.cfAbstr'' || || 1
|-
|Subject ''cfResPubl.cfKeyw; cfResPubl.cfResPubl_Class''||cfResPublKeyw may contain free-text keywords (multiple keywords can be included in one instance of the cfResPublKeyw field as a semi-colon separated list).
cfResPubl_Class may contain subject classification according to a controlled vocabulary. No single specific controlled vocabulary is enforced by the guidelines.
|| 0..N
|-
| Languague ''cfResPubl.ResPubl_Class''||Use ISO 639-x, where x can be 1, 2 or 3. Best Practice: use ISO 639-3. If ISO 639-2 and 639-1 are sufficient for the contents of a CRIS data source they can be used alternatively. Since there is a unique mapping this can be done during an aggregation process.
|| 1
|-
| Publication Types ''cfResPubl.cfResPubl_Class''||The range of allowed values is limited to the following controlled vocabulary:
* '''Book'''
* '''Book Review'''
* '''Book Chapter Abstract'''
* '''Book Chapter Review'''
* '''Inbook'''
* '''Anthology'''
* '''Monograph'''
* '''Referencebook'''
* '''Textbook'''
* '''Encyclopedia'''
* '''Manual'''
* '''Otherbook'''
* '''Journal'''
* '''Journal Issue'''
* '''Journal Article'''
* '''Journal Article Abstract'''
* '''Journal Article Review'''
* '''Conference Proceedings'''
* '''Conference Proceedings Article'''
* '''Conference Abstract'''
* '''Conference Poster'''
* '''Letter'''
* '''Letter to Editor'''
* '''PhD Thesis'''
* '''Doctoral Thesis'''
* '''Supervised Student Publications'''
* '''Report'''
* '''Short Communication'''
* '''Poster'''
* '''Presentation'''
* '''Newsclipping'''
* '''Commentary'''
* '''Annotation'''
* '''Transliteration'''
* '''Translation'''
* '''Authored Book'''
* '''Edited Book'''
* '''Chapter in Book'''
* '''Scholarly Edition'''
* '''Conference Contribution'''
* '''Working Paper'''
* '''Research Report for external body'''
* '''Confidential Report (for external body)'''
* '''Encyclopedia Entry'''
* '''Magazine Article'''
* '''Dictionary Entry'''
* '''Online Resource'''
* '''Standard and Policy'''
as defined in CERIF Semantics “Output Types” scheme.
|| 1
|-
| OA Types ''cfResPubl.ResPubl_Class'' || The range of allowed values is limited to the following controlled vocabulary:

* info:eu-repo/semantics/closedAccess
* info:eu-repo/semantics/embargoedAccess
* info:eu-repo/semantics/restrictedAccess
* info:eu-repo/semantics/openAccess

as defined in the info:eu-repo-Access-Terms vocabulary (http://purl.org/eu-repo/semantics/#info-eu-repo-AccessRights).

If the material is licensed under a Creative Commons license then links should be provided to applicable Creative Commons licenses, e.g.:

http://creativecommons.org/licenses/zero/1.0/ <br/>
http://creativecommons.org/licenses/by/3.0/

In the case of embargoedAccess, the endDate of the classification specifies the embargo end date for the publication.
|| 1
|-
|||||
|-
!'''Relationship with'''!!'''Applicable Vocabularies'''!!
|-
|Person ''cfResPubl.cfPers_ResPubl''||The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Author''' <br/>
as defined in CERIF Semantics  “Person Output Contributions” scheme.
|| 0..N
|-
|Organisation ''cfResPubl.cfOrgUnit_ResPubl'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Author Institution''' <br/>
'''- Publisher Institution''' <br/>
as defined in CERIF Semantics  “Organisation Output Roles” scheme.
|| 0..N
|-
| Project ''cfResPubl.cfProj_ResPubl'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Originator''' <br/>
as defined in CERIF Semantics  “Project Output Roles” scheme. I.e. Publication has originator Project.
|| 0..N
|-
| Product (Dataset) ''cfResPubl.cResPubl_ResProd'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Relation''' <br/>
as defined in CERIF Semantics “Inter-Output Relations” scheme.
|| 0..N
|-
| Publication ''cfResPubl.cfResPubl_ResPubl'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Part''' <br/>
as defined in CERIF Semantics “Inter-Publication Relations” scheme.
''Note: Articles can be related with the journal they appear in using the cfResPubl_ResPubl link entity with the “Part” classification term (eda28bc1-34c5-11e1-b86c-0800200c9a66) with a clear direction from the article cfResPublId to the host journal cfResPublId2.''
|| 0..N
|}

===The CERIF XML Person Entity in the OpenAIRE context===
{| class="wikitable"
|-
! Person (cfPers)
|-
|The CERIF entity cfPers is used in the context of OpenAIRE to represent persons that are related with publications (e.g. authors, etc.), datasets (e.g. creators, maintainers, etc.) or projects (e.g. contact person for organisation in project).
|-
|}

{| class="wikitable"
|-
! Attributes !! Applicable Vocabularies !! Multiplicity
|-
| Internal Identifier ''cfPers.cfPersId'' || || 1
|-
| Federated Identifiers ''cfPers.cfFedId.cfFedId'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- ORCID''' <br/>
'''- ResearcherID''' <br/>
'''- ScopusAuthorID''' <br/>
'''- STAFFID''' <br/>
'''- DNR''' <br/>
'''- ISNI''' <br/>
as defined in CERIF Semantics “Identifier Types” scheme.
|| 0..N
|-
| First Names ''cfPers.cfPersName_Pers.cfPersName.cfFirstNames'' || The range of allowed values is limited to the following controlled vocabulary:
'''- Presented Name''' <br/>
'''- Short Name''' <br/>
'''- Passport Name''' <br/>
as defined in CERIF Semantics “Person Names” scheme.
|| 1
|-
| Family Name ''cfPers.cfPersName_Pers.cfPersName.cfFamilyName'' || The range of allowed values is limited to the following controlled vocabulary:
'''- Presented Name''' <br/>
'''- Short Name''' <br/>
'''- Passport Name''' <br/>
as defined in CERIF Semantics “Person Names” scheme.
|| 1..N
|-
| Nationality of Persons ''cfPers.cfPers_Class'' || ISO 3166-1 standard list of country codes || 0..1
|-
|||||
|-
! '''Relationship with''' !! '''Applicable  Vocabularies''' !!
|-
| Electronic Addresse(s) ''cfPers.cfPers_EAddr'' || The range of allowed values is limited to the following controlled vocabulary:<br/>
'''- Email''' <br/>
'''- Fax''' <br/>
'''- Phone''' <br/>
as defined in CERIF Semantics “Person Contact Details” scheme.
|| 1..N
|-
|Publications ''cfPers.cfPers_ResPubl'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Author''' <br/>
as defined in CERIF Semantics “Person Output Contributions” scheme.
|| 0..N
|-
| Products ''cfPers.cfPers_ResProd'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Creator''' <br/>
'''- Publisher''' <br/>
as defined in CERIF Semantics “Person Output Contributions” scheme.
|| 0..N
|-
| Project ''cfPers.cfProj_Pers''
||  The range of allowed values is limited to the following controlled vocabulary:<br/>
'''- Organisation Contact In Project''' <br/>
as defined in CERIF Semantics “Person Project Engagements” scheme.
|| 0..N
|-
| Organisation ''cfPers.Pers_OrgUnit.cfClassId'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Affiliation''' <br/>
as defined in CERIF Semantics “Person Organisation Roles” scheme.
|| 0..N
|-
|}

===The CERIF XML Organisation Entity in the OpenAIRE context===
{| class="wikitable"
|-
! Organisation (cfOrgUnit)
|-
|The CERIF entity ''cfOrgUnit'' is used in the context of OpenAIRE to represent research performing organizations producing research results and/or involved in funded projects (e.g. coordinators, participants) or funder organisations.
|-
|}

{| class="wikitable"
|-
! Attributes !! Applicable Vocabularies !! Multiplicity
|-
| Internal Identifier ''cfOrgUnit.cfOrgUnitId'' || || 1
|-
| Federated Identifiers ''cfOrgUnit.cfFedId.FedId'' || The range of allowed values is limited to the following controlled vocabulary:
'''- PIC''' <br/>
'''- INSTID''' <br/>
'''- UKPRN''' <br/>
'''- VAT''' <br/>
as defined in CERIF Semantics “Identifier Types” scheme.
|| 0..N
|-
| Legal short name ''cfOrgUnit.cfAcro'' ||  || 1
|-
| Legal name ''cfOrgUnit.cfName'' || || 1
|-
| Web site URL ''cfOrgUnit.cfURI'' || || 1
|-
| Organisation classification ''cfOrgUnit.cfOrgUnit_Class'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Higher Education''' <br/>
'''- Private non-profit''' <br/>
'''- Company''' <br/>
'''- Government''' <br/>
'''- SME''' <br/>
'''- Intergovernmental''' <br/>
'''- Research Institute''' <br/>
as defined in CERIF Semantics “Organisation Types” scheme.
|| 0..1
|-
| NUTS code classification ''cfOrgUnit.cfOrgUnit_Class'' || The range of allowed values is limited to the NUTS vocabulary (http://simap.europa.eu/codes-and-nomenclatures/codes-nuts/) || 0..N
|-
| Country ''cfOrgUnit.cfOrgUnit_Class'' || ISO 3166-1 standard list of country codes || 0..1
|-
|||||
|-
! '''Relationship with''' !! '''Applicable  Vocabularies''' !!
|-
| Project ''cfOrgUnit.cfProj_OrgUnit'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Coordinator''' <br/>
'''- Partner''' <br/>
'''- Contractor''' <br/>
'''- Funder''' <br/>
'''- Inkind-Contributor''' <br/>
'''- Applicant''' <br/>
as defined in CERIF Semantics “Organisation Project Engagements” scheme.
|| 0..N
|-
| Funding ''cfOrgUnit.cfOrgUnit_Fund'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Manager''' <br/>
'''- Contributor''' <br/>
'''- Contact''' <br/>
'''- Applicant''' <br/>
'''- Issuer''' <br/>
'''- Responsible''' <br/>
'''- Financier''' <br/>
as defined in CERIF Semantics “Organisation Project Engagements” and “Organisation Funding Roles” schemes.
|| 0..N
|-
| Person ''cfOrgUnit.cfPers_OrgUnit'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Affiliation''' <br/>
as defined in CERIF Semantics “Person Organisation Roles” scheme.
|| 0..N
|-
|}

=== The CERIF XML Project Entity in the OpenAIRE context===

{| class="wikitable"
|-
! Project (cfProj)
|-
| The CERIF entity cfProj in the context of OpenAIRE is used to represent funded projects.
|-
|}

{| class="wikitable"
|-
! Attributes !! Applicable Vocabularies !! Multiplicity
|-
| Internal Identifier ''cfProj.cfProjId'' || || 1
|-
| Federated Identifiers ''cfProj.FedId.cfFedId'' || The range of allowed values is limited to the following controlled vocabulary:
'''- Project Reference''' <br/>
as defined in CERIF Semantics “Identifier Types” scheme.
|| 0..N
|-
| Acronym ''cfProj.cfAcro'' ||  || 1
|-
| Title ''cfProj.cfTitle'' || || 1
|-
| Keywords ''cfProj.cfKeyw'' || || 0..N
|-
| Web site URL ''cfProj.cfURI'' || || 0..1
|-
| Start Date ''cfProj.cfStartDate'' || || 1
|-
| End Date ''cfProj.cfEndDate'' || || 1
|-
|Open Access Requirements ''cfProj.cfProj_Class'' ||''Note: The vocabulary term list is expected to be informed through feedback regarding Open Access mandates internationally.''
|| 0..1
|-
!'''Relationship with'''!!'''Applicable Vocabularies'''!!
|-
| Publication ''cfProj.Proj_ResPubl'' || The range of allowed values is limited to the following controlled vocabulary:<br/>
'''- Originator'''
as defined in CERIF Semantics “Project Output Roles” scheme. i.e. Dataset has originator Project.
|| 0..N
|-
| Product / Dataset ''cfProj.Proj_ResProd'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Originator''' <br/>
as defined in CERIF Semantics “Project Output Roles” scheme. i.e. Dataset has originator Project.
|| 0..N
|-
| Organisation ''cfProj.cfProj_OrgUnit'' || The range of allowed values is limited to the following controlled vocabulary (adopted from the CERIF Semantics 1.5): <br/>
'''- Coordinator''' <br/>
'''- Partner''' <br/>
'''- Contractor''' <br/>
'''- Funder''' <br/>
'''- Inkind-contributer''' <br/>
'''- Applicant''' <br/>
as defined in CERIF Semantics “Organisation Project Engagements” scheme.
|| 1..N
|-
| Person ''cfProj.Proj_Pers'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''OrganisationContactInProject'''
as defined in CERIF Semantics “Person Project Engagements” scheme.
|| 0..N
|-
| Funding ''cfProj.Proj_Fund'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Award''' <br/>
'''- Grant''' <br/>
'''- Contract''' <br/>
as defined in CERIF Semantics “Activity Funding Types” scheme.
|| 0..N
|}

=== The CERIF XML Funding Entity in the OpenAIRE context ===

{| class="wikitable"
|-
! Funding (cfFund)
|-
| The CERIF entity cfFunding ''cfFund'' in the context of OpenAIRE is used to represent funding programmes (e.g. EU funded or national programmes) including their structures. Funding programme structures are represented using the recursive cfFund_Fund link entity. cfProj_Fund links funding programmes with projects and cfOrgUnit_Fund links funding programmes with organisations (e.g. funders).
|-
|}

{| class="wikitable"
|-
! Attributes !! Applicable Vocabularies !! Multiplicity
|-
| Internal Identifier ''cfFund.cfFundId'' || || 1
|-
| Federated Identifiers ''cfFund.cfFedId.cfFedId'' || The range of allowed values is limited to the following controlled vocabulary:
'''- Grant Reference''' <br/>
as defined in CERIF Semantics “Identifier Types” scheme.
|| 0..N
|-
| Name ''cfFund.cfName'' ||  || 1
|-
| Description ''cfFund.cfDescr'' || || 1
|-
| Keywords ''cfFund.cfKeyw'' || || 0..N
|-
| Funding Classification ''cfFund.cfFund_Class'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Funding Programme''' <br/>
'''- Call''' <br/>
'''- Tender''' <br/>
'''- Gift''' <br/>
'''- Internal Funding''' <br/>
as defined in CERIF Semantics “Funding Source Types” scheme.
|| 0..N
|-
|||||
|-
!'''Relationship with'''!!'''Applicable Vocabularies'''!!
|-
| Organisation ''cfFund.cfOrgUnit_Fund'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Manager''' <br/>
'''- Contributor''' <br/>
'''- Contact''' <br/>
'''- Applicant''' <br/>
'''- Issuer''' <br/>
'''- Responsible''' <br/>
'''- Financier''' <br/>
as defined in CERIF Semantics “Organisation Project Engagements” and “Organisation Funding Roles” schemes.
|| 0..N
|-
| (Recursive) Funding ''cfFund.cfFund_Fund'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Part'''  <br/>
as defined in CERIF Semantics “Inter-Funding Relations” scheme.
|| 1..N
|-
| Relationship with Project ''cfFund.Proj_Fund'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Award''' <br/>
'''- Grant''' <br/>
'''- Contract''' <br/>
as defined in CERIF Semantics “Activity Funding Types” scheme.
|| 0..N
|-
|}

=== The CERIF XML Service Entity in the OpenAIRE context ===


{| class="wikitable"
|-
! Service (cfSrv)
|-
| The CERIF entity cfService cfSrv in the context of OpenAIRE can be used (a) to provide information for the CERIF-compliant system that exposes data to OpenAIRE in CERIF XML and (b) in relation to federated identifiers (e.g. for persons, projects, organisations), in particular to identify the service that has generated each federated identifier. Federated identifiers are linked with the corresponding service using cfSrv.FedId_Srv. Services are linked with organisations through cfSrv.cfOrgUnit_Srv.
|-
|}

{| class="wikitable"
|-
! Attributes !! Applicable Vocabularies !! Multiplicity
|-
| Internal Identifier ''cfSrv.cfSrvId'' || || 1
|-
| Name ''cfSrv.cfName'' ||  || 1
|-
|||||
|-
! Relationship(s) with !! Applicable  Vocabularies !!
|-
| Organisation ''cfSrv.cfOrgUnit_Srv''|| The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Owner''' <br/>
as defined in CERIF Semantics “Organisation Research Infrastructure Roles” scheme.
|| 1
|-
|}

=== The CERIF XML Product Entity in the OpenAIRE context ===


{| class="wikitable"
|-
! Product / Dataset (cfResProd)
|-
| The CERIF entity cfResultProduct ''cfResProd'' is used in the context of OpenAIRE to represent research results that are classified as datasets. Datasets are linked with publications using cfResProd.cfResPubl_ResProd  and with funded project using cfResProd.cfProj_ResProd.
|-
|}

{| class="wikitable"
|-
! Attributes !! Applicable Vocabularies !! Multiplicity
|-
| Internal Identifier ''cfResProd.ResProdId'' || || 1
|-
| Federated Identifiers ''cfResProd.cfFedId'' || The range of allowed values is limited to the following controlled vocabulary, as in the OpenAIRE Guidelined for Data Archives - see https://guidelines.openaire.eu/wiki/OpenAIRE_Guidelines:_For_Data_Archives :
'''- ARK''' <br/>
'''- DOI''' <br/>
'''- Handle''' <br/>
'''- PURL''' <br/>
'''- URN''' <br/>
'''- URL''' <br/>
|| 0..N
|-
| Name ''cfResProd.cfName'' ||  || 1
|-
| Description ''cfResProd.cfDescr'' ||  || 1
|-
| Languague ''cfResProd.ResProd _Class'' || Use ISO 639-x, where x can be 1,2 or 3. Best Practice: use ISO 639-3. If ISO 639-2 and 639-1 are sufficient for the contents of a CRIS data source they can be used alternatively. Since there is a unique mapping this can be done during an aggregation process. || 1
|-
| License Types ''cfResProd.ResProd_Class'' || Use terms from the info:eu-repo-Access-Terms vocabulary, see http://purl.org/eu-repo/semantics/#info-eu-repo-AccessRights. The allowed values are the following: <br/>

* info:eu-repo/semantics/closedAccess
* info:eu-repo/semantics/embargoedAccess
* info:eu-repo/semantics/restrictedAccess
* info:eu-repo/semantics/openAccess

If the material is licensed under a Creative Commons license then you should provide links to applicable Creative Commons licenses, e.g.:<br/>

http://creativecommons.org/licenses/zero/1.0/ <br/>
http://creativecommons.org/licenses/by/3.0/
|| 1
|-
| Types of Products (Datasets) ''cfResProd.ResProd_Class'' || The range of allowed values is limited to the following controlled vocabulary (adopted from the OpenAIRE Guidelines for Data Archives): <br/>
'''- Collection''' <br/>
'''- Dataset'''  <br/>
'''- Event'''  <br/>
'''- Film'''  <br/>
'''- Image'''  <br/>
'''- InteractiveResource'''  <br/>
'''- Model''' <br/>
'''- PhysicalObject'''  <br/>
'''- Service'''  <br/>
'''- Software'''  <br/>
'''- Sound'''  <br/>
'''- Text''' <br/>
|| 1
|-
! Relationship(s) with !! Applicable  Vocabularies !!
|-
| Person ''cfResProd.cfPers_ResProd'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Creator''' <br/>
'''- Publisher''' <br/>
as defined in CERIF Semantics  “Person Output Contributions” scheme
|| 0..N
|-
| Organisation ''cfResProd.cfOrgUnit_ResProd'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Creator''' <br/>
'''- Publisher''' <br/>
as defined in CERIF Semantics “Organisation Output Contributions” scheme.
|| 0..N
|-
| Project ''cfProj.Proj_ResPro''|| The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Originator''' <br/>
as defined in CERIF Semantics “Project Output Roles” scheme. I.e. Dataset has originator Project.
|| 0..N
|-
| (Recursive) Product / Dataset ''cfResProd.cfResProd_ResProd'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Citation''' <br/>
'''- Supplement''' <br/>
'''- Continuation''' <br/>
'''- Metadata''' <br/>
'''- Version''' <br/>
'''- Part''' <br/>
'''- Reference''' <br/>
'''- Documentation''' <br/>
'''- Compilation''' <br/>
'''- Variant Form''' <br/>
'''- Originator''' <br/>
'''- Identic''' <br/>
as defined in CERIF Semantics “Inter-Product Relations”
|| 0..N
|-
| Publication ''cfResProd.ResPubl_ResProd'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Relation'''<br/>
as defined in CERIF Semantics  “Inter-Output Relations” scheme.
|| 0..N
|-
| Equipment ''cfResProd.ResProd_Equip'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Generation'''<br/>
as defined in CERIF Semantics “Infrastructure Output Relations” scheme.
|| 0..N
|-
|}

=== The CERIF XML Equipment Entity in the OpenAIRE context ===


{| class="wikitable"
|-
! Equipment (cfEquip)
|-
| The CERIF entity cfEquipment ''cfEquip'' is used in the context of OpenAIRE to represent equipment/devices that are used for the generation of data sets.
|-
|}

{| class="wikitable"
|-
! Attributes !! Applicable Vocabularies !! Multiplicity
|-
| Internal Identifier ''cfEquip.cfEquipId'' || || 1
|-
| Federated Identifiers ''cfEquip.cfFedId.cfFedId'' || The range of allowed values is limited to the following controlled vocabulary:<br/>
'''- UUID''' <br/>
'''- etc.''' <br/>
as defined in CERIF Semantics “Identifier Types” scheme.
|| 0..N
|-
| Name ''cfEquip.cfName'' ||  || 0..1
|-
| Acronym ''cfEquip.cfAcro'' ||  || 0..1
|-
| Description ''cfEquip.cfDescr'' ||  || 0..N
|-
|||||
|-
! Relationship(s) with !! Applicable  Vocabularies !!
|-
| Dataset ''cfEquip.cfResProd_Equip''|| The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Generation''' <br/>
as defined in CERIF Semantics “Infrastructure Output Relations” scheme.
|| 1..N
|-
|}

=== The CERIF XML Electronic Address Entity in the OpenAIRE context ===


{| class="wikitable"
|-
! Electronic Address (cfEAddr)
|-
| The CERIF entity cfElectronicAddress cfEAddr is used in the context of OpenAIRE to represent.
|-
|}

{| class="wikitable"
|-
! Attributes !! Applicable Vocabularies !! Multiplicity
|-
| Internal Identifier ''cfEAddr.cfEAddrId'' || || 1
|-
| URI ''cfEAddr.cfURI'' || || 1
|-
! Relationship(s) with !! Applicable  Vocabularies !!
|-
| Person ''cfEAddr.cfPers_EAddr'' || The range of allowed values is limited to the following controlled vocabulary: <br/>
'''- Email''' <br/>
'''- Fax''' <br/>
'''- Phone''' <br/>
as defined in CERIF Semantics “Person Contact Details” scheme.
|| 1..N
|-
|}

==Technical implementation guidelines ==

=== Data representation in CERIF XML ===

The CERIF XML style allowed is the one defined in CERIF 1.6 XML specification. The following rules apply – however we refer to the full specification for the details<ref>CERIF 1.6 XML Specification</ref>:

1. The CERIF data must be represented as descendants of a root XML element, “CERIF”. <br/>
2. Direct descendants of the CERIF elements must be only simple CERIF Entities CERIF 1.6 XML http://www.eurocris.org/Index.php?page=CERIF-1.6&t=1 (such as Person; Project; OrganisationUnit; ResultPublication; ResultProduct) not multi-lingual or link entities or federated identifiers. The list of CERIF Research Entities relevant to OpenAIREplus is the following:
::cfProject (''cfProj'')
::cfPerson (''cfPers'')
::cfOrganisationUnit (''cfOrgUnit'')
::cfResultPublication (''cfResPubl'')
::cfResultProduct (''cfResProd'')
::cfFunding (''cfFund'')
::cfService (''cfSrv'')
::cdEquipment (''cfEquip'')
::cfElectronicAddress (''cfEAddr'')
3. Each CERIF Research Entity in the CERIF XML file embeds multilingual attributes, link entities and federated identifiers. CERIF Research Entities themselves must not be embedded within another CERIF entity; they can be direct descendants of exclusively the root CERIF XML element. Only links to other entities are allowed to be embedded into CERIF Research entities. <br/>
4. Link entities must appear at both ends of a relationship. For example, if cfProject A is related to cfOrgUnit B, the linked entity cfProj_OrgUnit must appear embedded in the XML record of both cfProject A and cfOrgUnit B. Therefore, the XML element of every CERIF Research Entity instance must embed link entities for all the relationships to which the entity instance participates. <br/>
5. Each link entity contains, among others, the identifiers of a classification (term) that denotes the semantics of the relationship and the classification scheme (vocabulary) to whom the term belongs; neither the detailed specification of the classification nor detailed specification of the classification scheme. Every classification and classification scheme used in link entities should belong to the set of classifications and classification schemes that constitute the OpenAIRE CERIF Semantics specification (see Appendix X). Therefore, every identifier used for specifying semantics of link entities in the CERIF XML exposed by CRIS systems should be among the identifiers (UUIDs) contained in the OpenAIRE CERIF Semantics specification.<br/>
6. Referential integrity constraints for all relationships among entities should be satisfied in the CERIF XML data provided by the CRIS system. Therefore, it is required that all CERIF objects referenced in the linking relationships in the CERIF XML data are actually represented in the data provided by the same CRIS system. For example, consider the case of a relationship between cfOrgUnit A and cfProject B that is included in the source CRIS system. To accomplish this, the CERIF XML data exported by the CRIS system must contain:
::a. An XML record for cfOrgUnit A. This XML record must contain, as a nested XML element, the link entity cfProj_OrgUnit.
::b. An XML record for cfProj B. This XML record must contain, as a nested XML element, the link entity cfProj_OrgUnit.
It is worth noting that the two aforementioned XML records may be contained in distinct sets of XML records exported by the CRIS system through separate OAI-PMH sets (see Section “OpenAIRE OAI-PMH Set”).

===CERIF Semantic Layer link entities implementation in OpenAIRE CERIF XML===

The applicable vocabularies will be provided and thus recognised by the OpenAIRE infrastructure via identifiers (UUIDs) in the CERIF cfClass.cfClassId attributes’ values. Those specific vocabularies that must be used by CRIS systems harvested by OpenAIRE are specified in the tables of the section entitled “CRIS information elements relevant for OpenAIRE”.

===OAI-PMH for Harvesting===

OpenAIRE uses the OAI-PMH v2.0 protocol for harvesting metadata from CRIS systems.

==== Metadata Format ====

OpenAIRE expects metadata from CRIS systems to be encoded in the CERIF XML metadata format, as specialised for OpenAIRE. The following metadata prefix should be used: oai_cerif_openaire. For information on how to use the OpenAIRE CERIF XML please refer to the CERIF XML specification and the specialisations of CERIF XML defined in the present document.

==== OpenAIRE OAI-PMH Sets====
For harvesting the records relevant to OpenAIRE, the use of specific OAI-PMH sets at the local CRIS system is mandatory. The description and required characteristics of the sets are provided in the following table:
{| class="wikitable"
|-
! Description !! Required characteristics
|-
| The entire graph of CERIF entities in the source CRIS system of relevance to OpenAIRE. CERIF XML records for all vocabularies (classification schemes) and terms (classifications) used may be omitted, since they should be a subset of what is being specified in the OpenAIRE CERIF Semantics specification. || '''setName''': OpenAIRE_CRIS
'''setSpec''': openaire_cris
|-
|The list of CERIF XML records for persons with embedded multi-lingual entities, federated identifiers and link entities and for associated electronic addresses. || '''setName''': OpenAIRE_CRIS_persons
'''setSpec''': openaire_cris_persons
|-
| The list of CERIF XML records for projects with embedded multi-lingual entities, federated identifiers and link entities. || '''setName''': OpenAIRE_CRIS_projects
'''setSpec''': openaire_cris_projects
|-
| The list of CERIF XML records for organisation units with embedded multi-lingual entities, federated identifiers and link entities. || '''setName''': OpenAIRE_CRIS_orgunits
'''setSpec''': openaire_cris_orgunits
|-
| The list of CERIF XML records for funding with embedded multi-lingual entities, federated identifiers and link entities. || '''setName''': OpenAIRE_CRIS_funding
'''setSpec''': openaire_cris_funding
|-
| The list of CERIF XML records for publications with embedded multi-lingual entities, federated identifiers and link entities. || '''setName''': OpenAIRE_CRIS_publications
'''setSpec''': openaire_cris_publications
|-
| The list of CERIF XML records for datasets with embedded multi-lingual entities, federated identifiers and link entities and for associated equipment. || '''setName''': OpenAIRE_CRIS_datasets
'''setSpec''': openaire_cris_datasets
|-
| The list of CERIF XML records for services with embedded multi-lingual entities, federated identifiers and link entities. || '''setName''': OpenAIRE_CRIS_services
'''setSpec''': openaire_cris_services
|}

Referential integrity constraints for all relationships among entities should be satisfied in the CERIF XML data provided by the CRIS system, as mentioned in the “Data representation in CERIF XML” sub-section above. This holds also for the case that entity instances related via link entities are retrieved through different OAI-PMH sets. For example, consider the case of a relationship between cfOrgUnit A and cfProject B that is included in the source CRIS system. To accomplish this, the CERIF XML data exported by the CRIS system must contain:
::a. An XML record for cfOrgUnit A. This XML record must contain, as a nested XML element, the link entity cfProj_OrgUnit. The XML record of cfOrgUnit A must be available through both sets '''''openaire_cris''''' and '''''openaire_cris_orgunits'''''.
::b. An XML record for cfProj B. This XML record must contain, as a nested XML element, the link entity cfProj_OrgUnit. The XML record of cfProj B must be available through both sets openaire_cris and openaire_cris_projects.
In case the two entity instances (cfOrgUnit A and cfProj B) are retrieved via the different sets '''''openaire_cris_orgunits''''' and '''''openaire_cris_projects''''', the OAI-PMH service provider – in this case the OpenAIRE infrastructure – should combine and check the information in the two different sets of XML records to validate the source data in terms of referential integrity.

===Transmission of CERIF XML as OAI-PMH payload===
OAI-PMH is a protocol for exposing information from data providers to clients (service providers). Data provided through OAI-PMH must be encoded in XML and is organised into a sequence of records. The protocol uses the resumption token mechanism to enable control over the flow of data from the data provider towards the service provider, for example, it allows the split of a large chunk of records into fragments of manageable size (e.g. 100 records). This helps avoid overload of both the data and service provider.

Data in CERIF CRIS systems follows a normalised graph structure. Therefore, the transmission of CERIF XML as OAI-PMH payload requires a mechanism of fitting the graph structure into a sequence of records. The CERIF XML structure should be decomposed into a sequence of XML records. Each OAI-PMH XML record should represent a single instance of a CERIF Research Entity, embedding multi-lingual entities, federated identifiers and link entities, but with no nested records for other CERIF Research Entity instances.

====Date stamps in CERIF XML records====
In OAI-PMH, selective harvesting based on last-update date stamps on records is possible, so that only records that have been modified since the last harvesting are retrieved. Due to considerations regarding not consistent and reliable mechanisms for setting date stamp values in certain source systems, OpenAIRE in the general case tends to avoid employing selective harvesting based on last update dates. If reliable mechanisms for setting date stamps are present in a source CRIS system, OpenAIRE may employ selective harvesting, for example in the case of very large data sources.

The following rules apply regarding setting values of date stamps for CERIF XML records exposed by CRIS systems to OpenAIRE via OAI-PMH:

Datestamps should be set by CRIS systems in records, based on the following last update principle: the date stamp should reflect the last date/time where any information contained within the record payload (e.g. entity fields, multilingual fields, federated identifiers, linked entities). Any such modification should result in a modification of the date stamp; under no circumstances can the date stamp be earlier than this date.

For example, we assume a CERIF XML record of type cfProj, containing:
# Entity fields (e.g. cfProj.cfAcro)
# Multilingual fields (e.g. cfProj.cfTitle)
# Federated identifiers (e.g. grant agreement number in the case of EU FP7 projects).
# Linked entities (e.g. link entities cfProj_OrgUnit denoting participation of organisations to the project)
Let us consider the database underlying the CRIS system from which the CERIF XML is exported. Example update cases of the cfProj instance information in the database are provided in the following list, along with the corresponding date stamp modifications of the cfProj CERIF XML record:
:a. cfProj.cfAcro is modified. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
:b. An existing cfProj.cfTitle instance is modified, e.g. update of cfProj.cfTitle. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
:c. A new cfProj.cfTitle is added to this cfProj instance (e.g. the project title in another language). The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the addition.
:d. An existing federated identifier instance referring to this cfProj instance is modified, e.g. update of the cfProj.cfFedId.startDate. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
:e. An existing federated identifier instance classification referring to this cfProj instance is modified, e.g. update of the cfFedId_Class.cfEndDate. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
:f. An existing cfFedId_Srv linked entity instance, concerning a federated identifier referring to this cfProj instance is modified, e.g. update of the cfFedId_Srv.cfStartDate. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
:g. An existing cfSrv instance is modified (e.g. cfSrv.cfURI). This particular cfSrv instance concerns a service that has issued a federated identifier referring to this cfProj instance. In this case, the date stamp of the respective cfProj CERIF XML record must NOT be updated to the date/time of the modification.
:h. A new federated identifier is added for this cfProj instance. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the addition.
:i. A new cfProj_OrgUnit instance is added to the database, linking the cfProj instance to an organisation that participates in the project. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the addition.
:j. An existing cfProj_OrgUnit link entity instance is modified (e.g.  cfProj_OrgUnit.cfStartDate). The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
:k. An existing cfOrgUnit instance is modified (e.g. cfOrgUnit.cfAcro). This particular cfOrgUnit instance concerns an organization that is a partner in the project and thus is already connected with the cfProj through a cfProj_OrgUnit linked entity. In this case, the date stamp of the respective cfProj CERIF XML record must NOT be updated to the date/time of the modification.

====Deleted records====
OpenAIRE does not require CRIS systems to provide information about deleted records via OAI-PMH. Therefore, it is acceptable for a  CRIS system exposing metadata records to the OpenAIRE infrastructure to provide any of the three levels of support of deleted records, as defined in the OAI-PMH 2.0 specification: '''“no”''', '''“persistent”''' or '''“transient”'''. As mandated in the OAI-PMH 2.0 specification, CRIS systems must declare the level of support of deleted records in the deletedRecord element of the ''Identify'' response.

==Comments==
<comments/>
