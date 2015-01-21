{{TOCright}}
== Introduction ==
=== Aim ===
OpenAIRE gathers together research output related to European funding streams, with the aim of supporting open science and tracking research impact. This content consists of open access publications and related contextual information such as datasets, supplementary material, and research/project information.

Two other sets of OpenAIRE guidelines exist for repository managers:
* OpenAIRE Guidelines for Literature Repositories 3.0
* OpenAIRE Guidelines for CRIS systems (CERIF standard) – In draft

The OpenAIRE Guidelines for Data Archive Managers 2.0 will provide instruction for data archive managers to expose their metadata in a way that is compatible with the OpenAIRE infrastructure. The metadata from data archives should be included in the OpenAIRE information space, and exposed when data are related to an open access publication e.g. a dataset cited by an article.
To access a pdf version the guidelines see here: http://dx.doi.org/10.5281/zenodo.6918

By implementing the OpenAIRE Guidelines, data archive managers are facilitating the creation of enhanced publications and building the stepping-stones for a linked data infrastructure for research.

Exposure and visibility of content from a range of European repositories will be significantly increased when a common and interoperable approach is taken as well as adhering to existing guidelines. OpenAIRE is happy to assist in adherence to these guidelines.  This compatibility will lead to future interoperability between research infrastructures, and structured metadata is of benefit to individual data repositories and the scholarly community at large.

=== DataCite ===
OpenAIRE has adopted the DataCite Metadata Schema as the basis for harvesting and importing metadata about datasets from data archives.

The core mission of DataCite is to build and maintain a sustainable framework that makes it possible to cite data through the use of persistent identifiers, DOIs.

OpenAIRE shares the goal of the DataCite Metadata Schema - to provide a domain agnostic metadata schema and provide interoperability through a small number of properties - making interoperability possible in the simplest manner possible and as a result keep the technical barriers for implementation as low as possible.

We would like to thank DataCite for their kind support and help making these OpenAIRE Guidelines for Data Archive Managers possible.

=== What's different ===
In this document you will find the needed properties to make your data archive compatible with the OpenAIRE infrastructure. OpenAIRE has adopted the DataCite Metadata Schema version 3.0 with some minor adjustments.

* OpenAIRE accepts other persistent identifier schemes and not only a DOI in 1.1 identifierType.
* OpenAIRE recommends exporting links to related publications and datasets (i.e. 12. RelatedIdentifier property and attributes are mandatory when applicable).
* OpenAIRE recommends using the 7. Contributor property to relate a dataset to funding information.
* DataCite optional properties 8. Date and 17. Description are mandatory in OpenAIRE.
* OpenAIRE enforces an encoding scheme on DataCite property 16. Rights.

== Acknowledgements & Contributors ==
=== Editors ===
* Mikael K. Elbæk (Technical University of Denmark)
* Lars Holm Nielsen (CERN, Switzerland)

=== Experts & Reviewers ===
* Samuele Kaplun (CERN, Switzerland)
* Paolo Manghi (CNR, Italy)
* Natalia Manola (University of Athens, Greece)
* Jochen Schirrwagen (University of Bielefeld, Germany)
* Birgit Schmidt (University of Goettingen,Germany)
* Mathias Lösch (University of Bielefeld, Germany)
* Frauke Ziedorn (DataCite, Germany)
* Pedro Principe (University of Minho, Portugal)
* Eloy Rodrigues (University of Minho, Portugal)
* Najla Rettberg (University of Goettingen, Germany)
* to be completed

== Versions ==
* 2.0 April 2014
Updated to DataCIte Metadata Schema v3.0
* 1.0 December 2012
Initial document

== OpenAIRE application of DataCite Metadata Schema ==
OpenAIRE builds on the DataCite Metadata Schema v3.0 by making some of the otherwise optional DataCite properties mandatory, as well as enforcing specific encoding schemes on the values of some DataCite properties. The table below details the differences from the DataCite Metadata Schema.

Within OpenAIRE the use of properties are either:
* mandatory (M) = the property must always be present in the metadata record. An empty property is not allowed.
* mandatory when applicable (MA) = when the property can be obtained it must be present in the metadata record
* recommended (R) = the use of the property is recommended
* optional (O) = the property may be used to provide complementary information about the resource

The recommended status is made primarily to encourage users to input certain properties when creating a metadata record to enhance services.

{| class="wikitable"
|-
| '''Important''':
|-
| The table below details only differences from the DataCite Metadata Schema v3.0. Please refer to the DataCite Metadata Schema v3.0 for definition of properties and their encoding schemes: http://schema.datacite.org/meta/kernel-3/index.html
|}


{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (if different from DataCite) <ref>Only differences to the DataCite Metadata Schema v3.0 are noted here. Please refer to encoding schemes and allowed values in http://schema.datacite.org/meta/kernel-3/index.html</ref>
|-
| 1 || Identifier || M || DOI (Digital Object Identifier) is preferred. The format should be “10.1234/foo”.
|-
| 1.1 || identifierType || M || Unlike DataCite, OpenAIRE allows for DOIs and other types of identifiers.

Controlled List:
Allowed values:

ARK
DOI
Handle
PURL
URN
URL

|-
| 2 || Creator || M || -
|-
| 2.1 || creatorName || M || -
|-
| 2.2 || nameIdentifier || R || OpenAIRE recommends including a nameIdentifier such as an ORCID or a ISNI if available.
|-
| 2.2.1 || nameIdentifierScheme || R || -
|-
| 2.2.2 || schemeURI || O || -
|-
| 3 || Title || M || -
|-
| 3.1 || titleType || O || -
|-
| 4 || Publisher || M || -
|-
| 5 || PublicationYear || M || -
|-
| 6 || Subject || R || Example
|-
| 6.1 || subjectScheme || O || -
|-
| 6.2 || schemeURI || O || -
|-
| 7 || Contributor || MA/O || OpenAIRE uses this property to allow unique and persistent identification of the funder who has funded wholly or partly the dataset described. This does not exclude also using this property for additional contributors as defined by DataCite Metadata Schema v3.0.

The property and sub-properties are only ''mandatory when applicable (MA)'' for describing funding information. Further use is ''optional (O)''.

Please refer to the section “Funding information” at the end of the table for a complete example of the use of ''7. Contributor, 7.1 contributorType, 7.2 contributorName, 7.3 nameIdentifier, 7.3.1 nameIdentifierScheme'' to provide funding information.

|-
| 7.1 || contributorType || MA/O || If 7. Contributor is used, then contributorType is mandatory.

''Controlled List''
Allowed values (in-complete):

Funder

Please see DataCite Metadata Schema v3.0 for all allowed values.

|-
| 7.2 || contributorName || MA/O || If 7. Contributor is used, then contributorType is mandatory.

Applicable only when contributorType is “Funder”:

Name of the funding entity. Example for European Commission funded research use “European Commission”, or for Wellcome Trust funded research use  “Wellcome Trust”. Specifically ''do not'' use the project acronym.

|-
| 7.3 || nameIdentifier || MA/O || Applicable only when contributorType is “Funder”:

An authoritative list of projects (See http://api.openaire.eu/oai_pmh?verb=ListRecords&set=projects&metadataPrefix=oaf )  is exposed by OpenAIRE through OAI-PMH, and available for all repository managers. Values will include the project name and projectID. The projectID equals the Grant Agreement identifier, and is defined by the info:eu-repo namespace term grantAgreement<ref>See http://purl.org/eu-repo/semantics/#info-eu-repo-GrantAgreementIdentifiers</ref>

The syntax is:
<code>info:eu-repo/grantAgreement/Funder/FundingProgram/ProjectID/[Jurisdiction]/[ProjectName]/[ProjectAcronym]/</code>

where:

* <code>Funder</code> refers to the funding origanization (e.g., EC for European Commission, WT for Wellcome Trust)
* <code>FundingProgramme</code> refers to a specific programme (e.g., FP7)
* <code>ProjectID</code> refers to a unique identifier in the scope of the funder (and maybe the programme), e.g. a grant agreement number.
* <code>Jurisdiction</code> refers to the authority granted to a formally constituted legal body (e.g. EU for European Union)
* <code>ProjectName</code> contains the full name of the project
* <code>ProjectAcronym</code> contains the project’s acronym.

For OpenAIRE compatibility, the elements in square brackets are optional. Repositories may choose to use only the old three-part namespace (<code>info:eu-repo/grantAgreement/Funder/FundingProgram/ProjectID</code>), or use the extended version with six parts.

Note: When omitting fields in the extended version, the number of fields must nevertheless be preserved by using “/”. A correct example for omitting the the <code>ProjectName</code> field would therefore look like this: <code>EC/FP7/12345/EU//OpenAIREplus</code>

|-
| 7.3.1 || nameIdentifierScheme || MA/O || If 7.3 nameIdentifier is used, nameIdentifierScheme is mandatory.

Applicable only when contributorType is “Funder”:

''Controlled List''
Allowed values:

info

|-
| 8 || Date || M || ''Mandatory'' property in OpenAIRE instead of ''recommended'' in DataCite. For encoding scheme, please refer to DataCite Metadata Schema v3.0 for details.
|-
| 8.1 || dateType || M || Use “Issued” for the date the resource is published or distributed. To indicate the end of an embargo period, use “Available”. To indicate the start of an embargo period, use “Accepted”.

DataCite v3.0 further recommends use of “Created” and “Submitted”.

Further dateTypes may be specified. Please refer to DataCite Metadata Schema v3.0 for details.

|-
| 9 || Language || R || -
|-
| 10 || ResourceType || R || OpenAIRE strongly recommends use of ResourceType and the sub-property resourceTypeGeneral.
|-
| 10.1 || resourceTypeGeneral || R || -
|-
| 11 || AlternateIdentifier || O || -
|-
| 11.1 || alternateIdentifierType || O || -
|-
| 12 || RelatedIdentifier || MA || ''Mandatory when applicable'' property in OpenAIRE instead of recommended in DataCite.

Please refer to the section “Related publications and datasets information” below for specific details on how to link datasets and publications.

|-
| 12.1 || relatedIdentifierType || MA || -
|-
| 12.2 || relationType || MA || ''Controlled List''
Allowed values (recommended ones, please refer to DataCite Metadata Schema v2.2 for a complete list)

<u>IsCitedBy</u> (indicates that B includes A in a citation)
Cites (indicates that A includes B in a citation)
<u>IsSupplementTo</u> (indicates  that A is a supplement to B)
<u>isSupplementedBy</u> (indicates that B is a supplement to A)
<u>IsPartOf</u> (indicates A is a portion of B; may be used for elements of a series)
HasPart</u> (indicates A includes the part B)
<u>IsNewVersionOf</u> (indicates A is a new edition of B, where the new edition has been modified or updated)
<u>IsPreviousVersionOf</u> (indicates A is a previous edition of B)

'''Note''': ''Cites'' and ''IsCitedBy'' is specifically for when a publication/dataset directly cites another publication/dataset in its references, whereas ''References'' and ''IsReferencedBy'' is for when a dataset/publication is used as a source of information without a direct citation.

OpenAIRE encourages including minimum one of above listed relation types, but allows usage of all DataCite’s relation types.

|-
| 12.3 || relatedMetadataSchema || O || -
|-
| 12.4 || schemeURI || O || -
|-
| 12.5 || schemeType || O || -
|-
| 13 || Size || O || -
|-
| 14 || Format || O || -
|-
| 15 || Version || O || -
|-
| 16 || Rights || MA || ''Mandatory when applicable'' property in OpenAIRE instead of optional in DataCite.

Free text (see 16.1 rightsURI).

OpenAIRE uses this property to explicit declare the access right of the resource via 16.1 rightsURI. This does not exclude also using 16. Rights property for additional rights statements as defined by DataCite Metadata Schema v3.0. In particular OpenAIRE also recommends including license information if available.

Please refer to the section “Access right and license information” below for a full example of how to declare access right and license information.

|-
| 16.1 || rightsURI || MA || ''Mandatory when applicable'' property in OpenAIRE instead of optional in DataCite.

Use terms from the info:eu-repo-Access-Terms vocabulary<ref>See http://purl.org/eu-repo/semantics/#info-eu-repo-AccessRights </ref>. The values are
* <code>info:eu-repo/semantics/closedAccess</code>
* <code>info:eu-repo/semantics/embargoedAccess</code>
* <code>info:eu-repo/semantics/restrictedAccess</code>
* <code>info:eu-repo/semantics/openAccess</code>

This property may also be used to explicitly declare the license for the resource.

Please refer to the section “Access right and license information” below for a full example of how to declare access right and license information.
|-
| 17 || Description || MA || ''Mandatory when applicable'' property in OpenAIRE instead of optional in DataCite.
|-
| 17.1 || descriptionType || MA || If 17. Description is used, then descriptionType is mandatory.

Use of "Abstract" is ''mandatory when applicable'' in OpenAIRE instead of recommended in DataCite.

Further descriptionType values may be specified. Please refer to DataCite Metadata Schema v3.0 for details.
|-
| 18 || GeoLocation || R || -
|-
| 18.1 || geoLocationPoint || R || -
|-
| 18.2 || geoLocationBox || R || -
|-
| 18.3 || geoLocationPlace || R || -
|-
|}
The OpenAIRE Guidelines for Data Archive Managers are built on the DataCite Metadata Schema <ref>DataCite Metadata Schema version 3.0: http://schema.datacite.org/meta/kernel-3/index.html</ref>. The following properties are described in further detail to make full integration into the OpenAIRE information space and allow OpenAIRE to make links between publications and datasets; datasets and funding information.

== Access rights and license information ==
OpenAIRE uses the access rights to enable a better user experience by declaring the access rights clear and explicit in the portal. Access rights are specified using the ''16. Rights'' property. Please see encoding scheme in the section above.

An example:
<code>
  <rightsList>
    <rights rightsURI=”info:eu-repo/semantics/openAccess” />
  </rightsList>
</code>

OpenAIRE further recommends including license information if available:

<code>
  <rightsList>
    <rights rightsURI=”info:eu-repo/semantics/openAccess” />
    <rights rightsURI=”http://creativecommons.org/licenses/by/4.0/”>
      Creative Commons Attribution 4.0 International
    </rights>
  </rightsList>
</code>

== Funding information ==
One of OpenAIRE’s main goals is to link research output to (EC) research funding. The following application of the contributor property allows unique and persistent identification of the funder who has funded wholly or partly the dataset described.

The following properties are mandatory when applicable to provide funding information: ''7. Contributor; 7.1 contributorType; 7.2 contributerName; 7.3 nameIdentifier; 7.3.1 nameIdentifierScheme'':

An example for linking a research output to the OpenAIREplus FP7 project:
<code>
 <contributor contributorType='''"Funder"'''>
  <contributorName><br>'''European Commission'''
  </contributorName>
  <nameIdentifier nameIdentifierScheme='''"info"'''><br>'''info:eu-repo/grantAgreement/EC/FP7/282896'''
  </nameIdentifier>
 </contributor>
</code>

== Related publications and datasets information ==
OpenAIRE '''harvests all datasets''' from a data repository, but '''exposes only certain''' datasets in the OpenAIRE portal. See the section “OpenAIRE OAI Set” below for specific details of which datasets are exposed.

For example, datasets related to publication will be exposed in the OpenAIRE portal. The link between the dataset and publication may be explicit defined, as described in this section below, or automatically inferred by the OpenAIRE infrastructure. If the link is explicit defined, the dataset will be exposed in the OpenAIRE portal '''within 1-2 days after harvesting''' (a repository is harvested once a week on average). If the link is automatically inferred by the OpenAIRE infrastructure it may take '''up to a month after harvesting''' before the dataset is exposed in the OpenAIRE portal. It is thus ''mandatory when applicable'' to provide links to related publications and datasets when these links are available in the repository, and thereby ensure faster exposure of the dataset in the OpenAIRE portal.

=== Related identifiers ===
DataCite Metadata Schema allows linking publications and datasets by use of persistent identifiers to uniquely identify the resource being described (A) typically a dataset but not limited to that, and the related resource (B) in the case of OpenAIRE typically a publication or a dataset.

Related publications/datasets must have the following properties: ''12. RelatedIdentifier, 12.1 relatedIdentifierType, 12.2 relationType''

An example:
<code>
 <relatedIdentifier<br>relatedIdentifierType='''"DOI"'''  relationType='''"IsCitedBy"'''>
 '''10.1234/bar'''
 </relatedIdentifier>
</code>

== Embargo date information ==
For OpenAIRE two main types of dates are relevant. When the data were made available, published or uploaded to a formal database, this is the date the data were ''Issued''.

Sometimes data may be embargoed for a period; this information should be managed by the data provider and expressed by exporting an ''Available'' date to indicate the end of an embargo period and an ''Accepted'' date to indicate the start of an embargo period.

An example:
<code>

 <dates>
  <date dateType='''"Issued"'''>2011-12-01</date>
 </dates>

</code>

An embargo example:
<code>

 <dates>
  <date dateType='''"Accepted"'''>2011-12-01</date>
  <date dateType='''"Available"'''>2012-12-01</date>
 </dates>

</code>

== Use of OAI-PMH ==
OpenAIRE uses the OAI-PMH v2.0 protocol for harvesting dataset metadata.

=== Metadata Format ===
OpenAIRE expects metadata to be encoded in the DataCite metadata format (metadataPrefix <code>oai_datacite</code>) . For information on how to use the individual DataCite properties, please refer to the section “OpenAIRE application of DataCite Metadata Schema” above.

=== OpenAIRE OAI Set ===
A specific OAI-Set at the local repository should be configured to select records relevant to OpenAIRE for harvesting. The following characteristics of the set are recommended:
{| class="wikitable"
|-
! setName !! setSpec<sup>*</sup>
|-
| OpenAIRE_data || openaire_data
|-
|}

<sup>*</sup>A harvester only uses the setSpec request to perform selective harvesting. The letters must be in small caps.

=== Set content ===
The specific content of the <code>openaire_data</code> set is to be determined at the local repository. OpenAIRE will '''harvest all datasets''' from the <code>openaire_data</code> set, but will '''only expose datasets fulfilling at least one''' of the following criteria in the OpenAIRE portal:
* The dataset is outcome of a funded research project identified by a project identifier (see section “Funding information” above).
* The dataset is linked with a publication in the OpenAIRE information space (see section “Related publications and datasets information” above).

Both criteria above may be automatically inferred by the OpenAIRE infrastructure.

Specifically a data repository may insert a dataset without funding information or link to a related publication in the <code>openaire_data</code> set. If later a publication harvested from a literature repository links to the dataset, the dataset will be exposed in the OpenAIRE portal. If either the literature repository or the data repository explicitly links the publication and dataset (see section ”Related publications and datasets information”), the dataset will normally be exposed in the OpenAIRE portal '''within 1-2 days after harvesting''' (repositories are harvested on average once a week). If the OpenAIRE infrastructure automatically has to infer the link between the publication and the dataset, it may take '''up to a month after harvesting''' before the dataset is exposed in the OpenAIRE portal.

 
==Comments==
<comments/>
