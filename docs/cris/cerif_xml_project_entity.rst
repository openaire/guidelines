.. _c:projectentity:

4. Project Entity (cfProj)
==================================

The CERIF entity cProject *cfProj* in the context of OpenAIRE is used to represent funded projects.

Attributes
----------

Internal Identifier
^^^^^^^^^^^^^^^^^^^

(occurences: 1)

*cfProj.cfProjId*

Federated Identifiers
^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..N)

*cfProj.cfFedId.cfFedId* (where the type of identifier is given through *cfProj.cfFedId.cfFedId_Class*)

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Project Reference**
* **URL (project web site URL)**

as defined in CERIF Semantics “Identifier Types” scheme.

Acronym 
^^^^^^^

(occurences: 1)

*cfProj.cfAcro*

Title
^^^^^

(occurences: 1)

*cfProj.cfTitle*

Keywords 
^^^^^^^^

(occurences: 0..N)

*cfProj.cfKeyw*

Start Date
^^^^^^^^^^

(occurences: 1)

*cfProj.cfStartDate*

End Date
^^^^^^^^

(occurences: 1)

*cfProj.cfEndDate*

Open Access Requirements
^^^^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..1)

*cfProj.cfProj_Class*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **OA mandated**
* **OA not mandated**

as defined in the “OpenAIRE Open Access Requirements” scheme.

.. note::
   The vocabulary term list is expected to be extended in the future through feedback regarding Open Access mandates internationally.

Relationship(s) with
--------------------

Publication 
^^^^^^^^^^^

(occurences: 0..N)

*cfProj.Proj_ResPubl*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Originator**

as defined in CERIF Semantics “Project Output Roles” scheme. i.e. Publication has originator Project.

Product / Dataset
^^^^^^^^^^^^^^^^^

(occurences: 0..N)

*cfProj.cfProj_ResProd*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Originator**

as defined in CERIF Semantics “Project Output Roles” scheme. i.e. Dataset has originator Project.

Organisation
^^^^^^^^^^^^

(occurences: 1..N)

*cfProj.cfProj_OrgUnit*

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

Person
^^^^^^

(occurences: 0..N)

*cfProj.Proj_Pers*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Organisation Contact In Project**

as defined in the “OpenAIRE Person Organisation Project Relationships” scheme.

Funding
^^^^^^^

(occurences: 0..N)

*cfProj.Proj_Fund*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Award**
* **Grant**
* **Contract**

as defined in CERIF Semantics “Activity Funding Types” scheme.


