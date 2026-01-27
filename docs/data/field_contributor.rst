.. include:: ../common/replacements.rst

.. _d:contributor:

7. Contributor (MA/O)
---------------------
The institution or person responsible for collecting, managing, distributing, or otherwise contributing to the development of the resource (occurrences: 0-n).

**Allowed values, examples, other constraints**

Note: DataCite infrastructure supports up to between 8000 - 10000 names. For name lists above that size, consider attribution via linking to the related metadata.

.. note::

   OpenAIRE uses this property to allow unique and persistent identification of the funder who has funded wholly or partly the dataset described. This does not exclude also using this property for additional contributors as defined by DataCite Metadata Schema |datacitever|.

   The property and sub-properties are only *mandatory when applicable (MA)* for describing funding information. Further use is *optional (O)*.

   Please refer to the section :ref:`fundinginfo` for a complete example of the use of :ref:`d:contributor`, :ref:`d:contributortype`, :ref:`d:contributorname`, :ref:`d:contributor_nameidentifier` and :ref:`d:contributor_nameidentifierscheme` to provide funding information.

.. _d:contributortype:

7.1 contributorType (MA/O)
~~~~~~~~~~~~~~~~~~~~~~~~~~
The type of contributor of the resource (occurrences: 1).

**Allowed values, examples, other constraints**

If :ref:`d:contributor` is used, then :ref:`d:contributortype` is mandatory.

*Controlled List Values:*

* ContactPerson
* DataCollector
* DataCurator
* DataManager
* Distributor
* Editor
* Funder
* HostingInstitution
* Producer
* ProjectLeader
* ProjectManager
* ProjectMember
* RegistrationAgency
* RegistrationAuthority
* RelatedPerson
* Researcher
* ResearchGroup
* RightsHolder
* Sponsor
* Supervisor
* WorkPackageLeader
* Other

.. _d:contributorname:

7.2 contributorName (MA/O)
~~~~~~~~~~~~~~~~~~~~~~~~~~
The name of the contributor (occurrences: 1).

**Allowed values, examples, other constraints**

If :ref:`d:contributor` is used, then :ref:`d:contributorname` is mandatory.

Examples: Patel, Emily; Doe, John

The personal name format may be: family, given. Non-roman names should be transliterated according to the `ALA-LC <http://www.loc.gov/catdir/cpso/roman.html>`_ schemes.

.. note::

   Applicable only when contributorType is “Funder”:

   Name of the funding entity. Example for European Commission funded research use ``European Commission``, or for Wellcome Trust funded research use ``Wellcome Trust``. Specifically do not use the project acronym.

.. _d:contributor_nameidentifier:

7.3 nameIdentifier (MA/O)
~~~~~~~~~~~~~~~~~~~~~~~~~
Uniquely identifies an individual or legal entity, according to various schemes (occurrences: 0-1).

**Allowed values, examples, other constraints**

The format is dependent upon scheme.

.. note::

   Applicable only when contributorType is “Funder”:

   .. include:: ../common/projectid.rst

.. _d:contributor_nameidentifierscheme:

7.3.1 nameIdentifierScheme (MA/O)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The name of the name identifier scheme (occurrences: 1).

**Allowed values, examples, other constraints**

If :ref:`d:contributor_nameidentifier` is used, :ref:`d:contributor_nameidentifierscheme` is mandatory.

Examples:`ORCID <http://orcid.org/>`_, `ISNI <http://www.isni.org/>`_, `FundRef <http://www.crossref.org/fundref/>`_.

.. note::

   Applicable only when contributorType is “Funder”:

   *Controlled List Values:*

   * info

.. _d:contributor_schemeuri:

7.3.2 schemeURI (O)
~~~~~~~~~~~~~~~~~~~
The URI of the name identifier scheme (occurrences: 0-1).

**Allowed values, examples, other constraints**

Examples:

* http://www.isni.org
* http://orcid.org
* http://www.crossref.org/fundref/

.. _d:contributor_affiliation:

7.4 affiliation (O)
~~~~~~~~~~~~~~~~~~~
The organizational or institutional affiliation of the contributor (occurrences: 0-n).

**Allowed values, examples, other constraints**

Free text.

Example
~~~~~~~

.. include:: examples/funding.rst
