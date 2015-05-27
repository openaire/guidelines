.. _c:organisationentity:

3. Organisation Entity (cfOrgUnit)
==================================

The CERIF entity cfOrganisationUnit *cfOrgUnit* is used in the context of OpenAIRE to represent research performing organizations producing research results and/or involved in funded projects (e.g. coordinators, participants) or funder organisations.

Attributes
----------

Internal Identifier
^^^^^^^^^^^^^^^^^^^

(occurences: 1)

 *cfOrgUnit.cfOrgUnitId*

Federated Identifiers
^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..N)

*cfOrgUnit.cfFedId.cfFedId* (where the type of identifier is given through *cfOrgUnit.cfFedId.cfFedId_Class*)

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **PIC**
* **INSTID**
* **UKPRN**
* **URL (organisation web site URL)**
* **VAT Identification Number**

as defined in CERIF Semantics “Identifier Types” scheme.

Legal short name
^^^^^^^^^^^^^^^^

(occurences: 1)

*cfOrgUnit.cfAcro*

Legal name 
^^^^^^^^^^

(occurences: 1)

*cfOrgUnit.cfName*

Organisation classification
^^^^^^^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..1)

*cfOrgUnit.cfOrgUnit_Class*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Higher Education**
* **Private non-profit**
* **Company**
* **Government**
* **SME**
* **Intergovernmental**
* **Research Institute**

as defined in CERIF Semantics “Organisation Types” scheme.

NUTS code classification
^^^^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..N)

*cfOrgUnit.cfOrgUnit_Class*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the NUTS vocabulary (http://simap.europa.eu/codes-and-nomenclatures/codes-nuts/)

Country
^^^^^^^

(occurences: 0..1)

*cfOrgUnit.cfOrgUnit_Class*

Applicable Vocabularies
"""""""""""""""""""""""

Use ISO 3166-1 standard list of country codes.

Relationship(s) with
--------------------

Project
^^^^^^^

(occurences: 0..N)

*cfOrgUnit.cfProj_OrgUnit*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Coordinator**
* **Partner**
* **Contractor**
* **Funder**
* **Inkind-Contributor**
* **Applicant**

as defined in CERIF Semantics “Organisation Project Engagements” scheme.

Funding
^^^^^^^

(occurences: 0..N)

*cfOrgUnit.cfOrgUnit_Fund*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Manager**
* **Contributor**
* **Contact**
* **Applicant**
* **Issuer**
* **Responsible**
* **Financier**
* **Funder**

as defined in CERIF Semantics “Organisation Project Engagements” and “Organisation Funding Roles” schemes.

Person
^^^^^^

(occurences: 0..N)

*cfOrgUnit.cfPers_OrgUnit*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Affiliation**

as defined in CERIF Semantics “Person Organisation Roles” scheme.

Publication
^^^^^^^^^^^

(occurences: 0..N)

*cfOrgUnit.cfOrgUnit_ResPubl*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Author Institution**
* **Editor Institution**
* **Publisher Institution**

as defined in CERIF Semantics  “Organisation Output Roles” scheme.

