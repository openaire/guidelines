==Contributor==
{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (if different from DataCite)
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

|}

==Definition==

===Contributor===
The institution or person responsible for collecting, creating, or otherwise contributing to the development of the dataset.

'''Occurrences''': 0-n

===contributorType (attribute)===
The type of contributor of the resource.

'''Occurrences''': Required

===contributorName (child) ===
The name of the contributor.

'''Occurrences''': 1

===nameIdentifier (child) ===
Uniquely identifies an individual or legal entity, according to various schemes.

'''Occurrences''': 0-1

===nameIdentifierScheme (attribute) ===
The name and/or the URL of the name identifier scheme.

'''Occurrences''': Required

==Allowed values (DataCite)==

===Contributor===
May be a corporate/institutional or personal name. The personal name format should be:
family, given.Non‐roman names should be transliterated according to the ALA‐LC schemes found at http://www.loc.gov/catdir/cpso/roman.html

===contributorType===
''Controlled list''
Allowed values:
* ContactPerson
* DataCollector
* DataManager
* Distributor
* Editor
* Funder
* HostingInstitution
* Producer
* ProjectLeader
* ProjectMember
* RegistrationAgency
* RegistrationAuthority
* RelatedPerson
* Researcher
* RightsHolder
* Sponsor
* Supervisor
* WorkPackageLeader

===contributorName===
Examples: Patel, Emily; Doe, John

===nameIdentifier===
The format is dependent upon scheme

===nameIdentifierScheme===
Examples are ORCID, ISNI

==OpenAIRE==
OpenAIRE have a specific use of the ''Contributor'' property to identify links to funding steams.

One of OpenAIRE’s main goals is to link research output to (EC) research funding. The following application of the contributor property allows unique and persistent identification of the funder who has funded wholly or partly the dataset described.

The following properties are mandatory when applicable to provide funding information: ''7. Contributor; 7.1 contributorType; 7.2 contributorName; 7.3 nameIdentifier; 7.3.1 nameIdentifierScheme'':

An example for linking a research output to the OpenAIREplus FP7 project:
<code>
 <contributor contributorType='''"Funder"'''>
  <contributorName><br>'''European Commission'''
  </contributorName>
  <nameIdentifier nameIdentifierScheme='''"info"'''><br>'''info:eu-repo/grantAgreement/EC/FP7/282896'''
  </nameIdentifier>
 </contributor>
</code>


==XML example==
Besides the use of ''Contributor'' for identifying funding steams a more general use of the property is shown below.

<code>
 <contributors>
  <contributor contributorType="DataManager">
   <contributorName>PANGAEA</contributorName>
  </contributor><contributor contributorType="ContactPerson">
   <contributorName>Doe, John</contributorName>
    <nameIdentifier nameIdentifierScheme="ORCID">xyz789</nameIdentifier>
  </contributor>
 </contributors>
</code>

==Comments==
<comments/>
