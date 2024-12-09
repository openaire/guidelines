An authoritative `list of projects <http://api.openaire.eu/oai_pmh?verb=ListRecords&set=projects&metadataPrefix=oaf>`_ is exposed by OpenAIRE through OAI-PMH, and available for all repository managers. Values include the project name and project ID. The projectID equals the Grant Agreement identifier, and is defined by the `info:eu-repo namespace <http://purl.org/eu-repo/semantics/#info-eu-repo-GrantAgreementIdentifiers>`_ term grantAgreement.

The syntax is::

   info:eu-repo/grantAgreement/Funder/FundingProgram/ProjectID/
   [Jurisdiction]/[ProjectName]/[ProjectAcronym]

where:

* ``Funder`` refers to the funding organization (e.g., ``EC`` for European Commission, ``WT`` for Wellcome Trust)
* ``FundingProgramme`` refers to a specific programme (e.g., ``FP7`` for Framework Programme Seven, ``H2020`` for Horizon 2020, ``HE`` for Horizon Europe )
* ``ProjectID`` refers to a unique identifier in the scope of the funder (and maybe the programme), e.g. a grant agreement number.
* ``Jurisdiction`` refers to the authority granted to a formally constituted legal body (e.g. ``EU`` for European Union)
* ``ProjectName`` contains the full name of the project
* ``ProjectAcronym`` contains the project’s acronym.

For OpenAIRE compatibility, the elements in square brackets are optional. The three-part namespace is *mandatory when applicable* (``info:eu-repo/grantAgreement/Funder/FundingProgram/ProjectID``), while the six-parts namespace is *recommended*.

When omitting fields in the extended version, the number of fields must be preserved by using ``/``. A correct example for omitting the the ``ProjectName`` field would therefore look like this: ``EC/FP7/12345/EU//OpenAIREplus``

If any of the field values contains a forward slash (``/``), it needs to be escaped using URL encoding (``%2F``). For instance, ``My/Project`` would be represented as ``My%2FProject``.
