== Field Name ==
Project Identifier
== DC Field ==
<code>dc:relation</code>

== Usage ==
''Mandatory when applicable''

== Usage Instruction ==
An authoritative list of projects (See http://api.openaire.eu/oai_pmh?verb=ListRecords&set=projects&metadataPrefix=oaf ) is exposed by OpenAIRE through OAI-PMH, and available for all repository managers. Values include the project name and project ID. The projectID equals the Grant Agreement identifier, and is defined by the info:eu-repo namespace term grantAgreement.

The syntax is:

<code>info:eu-repo/grantAgreement/Funder/FundingProgram/ProjectID /[Jurisdiction]/[ProjectName]/[ProjectAcronym]</code>

where:

* Funder refers to the funding origanization (e.g., EC for European Commission, WT for Wellcome Trust)
* FundingProgramme refers to a specific programme (e.g., FP7)
* ProjectID refers to a unique identifier in the scope of the funder (and maybe the programme), e.g. a grant agreement number.
* Jurisdiction refers to the authority granted to a formally constituted legal body (e.g. EU for European Union)
* ProjectName contains the full name of the project
* ProjectAcronym contains the project’s acronym.

For OpenAIRE compatibility, the elements in square brackets are optional. Repositories may choose to use the old three-part namespace (<code>info:eu-repo/grantAgreement/Funder/FundingProgram/ProjectID</code>) as specified in previous versions of the Guidelines, or use the extended version with six parts, which is recommended.

'''Note:''' If any of the field values contains a forward slash (<code>/</code>), it needs to be escaped using URL encoding (<code>%2F</code>). For instance, My/Project would be represented as <code>My%2FProject</code>.

== Do Not Confuse With ==
--
== Since ==
OpenAIRE Guidelines v1

== Examples ==
An example utilizing all six fields:
<pre>
<dc:relation>
  info:eu-repo/grantAgreement/EC/FP7/244909/EU/Making Capabilities Work/WorkAble
</dc:relation>
</pre>
An example for omitting the the ProjectName field (note that the number of slashes is correctly preserved):
<pre>
<dc:relation>
  info:eu-repo/grantAgreement/EC/FP7/283595/EU//OpenAIREplus
</dc:relation>
</pre>

A correct example using the old three-part form (discouraged):
<pre>
<dc:relation>
  info:eu-repo/grantAgreement/EC/FP7/244909
</dc:relation>
</pre>

==Comments==
<comments/>
