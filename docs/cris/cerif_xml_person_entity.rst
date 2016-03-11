.. _c:personentity:

2. Person Entity (cfPers)
=========================

The CERIF entity cfPerson *cfPers* is used in the context of OpenAIRE to represent persons that are related to publications (e.g. authors, etc.), datasets (e.g. creators, maintainers, etc.) or projects (e.g. contact person for organisation in project).

Attributes
----------

Internal Identifier
^^^^^^^^^^^^^^^^^^^

(occurences: 1)

 *cfPers.cfPersId*

Federated Identifiers
^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..N)

 *cfPers.cfFedId.cfFedId*
 (where the type of identifier is given through
 *cfPers.cfFedId.cfFedId_Class* )

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **ORCID**
* **ResearcherID**
* **ScopusAuthorID**
* **STAFFID**
* **DNR**
* **ISNI**

as defined in CERIF Semantics "Identifier Types" scheme.

First Names 
^^^^^^^^^^^

(occurences: 1)

*cfPers.cfPersName_Pers.cfPersName.cfFirstNames*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Presented Name**
* **Short Name**
* **Passport Name**

as defined in CERIF Semantics “Person Names” scheme.

Family Name
^^^^^^^^^^^

(occurences: 1..N)

*cfPers.cfPersName_Pers.cfPersName.cfFamilyNames*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Presented Name**
* **Short Name**
* **Passport Name**

as defined in CERIF Semantics “Person Names” scheme.

Nationality of Persons
^^^^^^^^^^^^^^^^^^^^^^

(occurences: 1..N)

*cfPers.cfPers_Class*

Applicable Vocabularies
"""""""""""""""""""""""

ISO 3166-1 standard list of country codes.

Relationship(s) with
--------------------

Electronic Addresse(s)
^^^^^^^^^^^^^^^^^^^^^^

(occurences: 1..N)

*cfPers.cfPers_EAddr*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Email**
* **Fax**
* **Phone**

as defined in CERIF Semantics “Person Contact Details” scheme.

Publications
^^^^^^^^^^^^

(occurences: 0..N)

*cfPers.cfPers_ResPubl*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Author**
* **Editor**

as defined in CERIF Semantics “Person Output Contributions” scheme.

Products 
^^^^^^^^

(occurences: 0..N)

*cfPers.cfPers_ResProd*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Creator**
* **Publisher**

as defined in CERIF Semantics “Person Output Contributions” scheme.

Project 
^^^^^^^

(occurences: 0..N)

*cfPers.cfProj_Pers*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Organisation Contact In Project**

as defined in the “OpenAIRE Person Organisation Project Relationships” scheme.

Organisation
^^^^^^^^^^^^

(occurences: 0..N)

*cfPers.Pers_OrgUnit.cfClassId*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Affiliation**

as defined in CERIF Semantics “Person Organisation Roles” scheme.


