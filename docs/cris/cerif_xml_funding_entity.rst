.. _c:fundingentity:

5. Funding Entity (cfFund)
==================================

The CERIF entity cfFunding *cfFund* in the context of OpenAIRE is used to represent funding programmes (e.g. EU funded or national programmes) including their structures. Funding programme structures are represented using the recursive cfFund_Fund link entity. cfProj_Fund links funding programmes with projects and cfOrgUnit_Fund links funding programmes with organisations (e.g. funders).

Attributes
----------

Internal Identifier
^^^^^^^^^^^^^^^^^^^

(occurences: 1)

 *cfFund.cfFundId*

Federated Identifiers
^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..N)

*cfFund.cfFedId.cfFedId* (where the type of identifier is given through *cfFund.cfFedId.cfFedId_Class*)

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Grant Reference**

as defined in CERIF Semantics “Identifier Types” scheme.

Name
^^^^

(occurences: 1)

*cfFund.cfName*

Description
^^^^^^^^^^^

(occurences: 1)

*cfFund.cfDescr*

Keywords
^^^^^^^^

(occurences: 0..N)

*cfFund.cfKeyw*

Funding Classification
^^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..N)

*cfFund.cfFund_Class*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Funding Programme**
* **Call**
* **Tender**
* **Gift**
* **Internal Funding**

as defined in CERIF Semantics “Funding Source Types” scheme.

Open Access Requirements
^^^^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..1)

*cfFund. cfFund_Class*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **OA mandated**
* **OA not mandated**

as defined in the “OpenAIRE Open Access Requirements” scheme.

.. note::
   The vocabulary term list is expected to be extended in the future through feedback regarding particular Open Access mandates internationally.

Relationship(s) with
--------------------

Organisation
^^^^^^^^^^^^

(occurences: 0..N)

*cfFund.cfOrgUnit_Fund*

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

(Recursive) Funding
^^^^^^^^^^^^^^^^^^^

(occurences: 0..N)

*cfFund.cfFund_Fund*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Part**

as defined in CERIF Semantics “Inter-Funding Relations” scheme.

Relationship with Project
^^^^^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..N)

*cfFund.Proj_Fund*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Award**
* **Grant**
* **Contract**

as defined in CERIF Semantics “Activity Funding Types” scheme.


