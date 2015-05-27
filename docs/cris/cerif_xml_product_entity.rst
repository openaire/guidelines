.. _c:productentity:

7. Product / Dataset Entity (cfResProd)
=======================================

The CERIF entity cfResultProduct *cfResProd* is used in the context of OpenAIRE to represent research results that are classified as datasets. The CERIF vocabulary also defines datasets at a more generic level as “Research Datasets and Databases” under “Output-Types”– the CERIF types are therefore provided as an applicable option below). Datasets are linked with publications using cfResProd.cfResPubl_ResProd  and with funded projects using the cfResProd.cfProj_ResProd link. 

Attributes
----------

Internal Identifier
^^^^^^^^^^^^^^^^^^^

(occurences: 1)

 *cfResProd.ResProdId*

Federated Identifiers
^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..N)

*cfResProd.cfFedId.cfFedId* (where the type of identifier is given through *cfResProd.cfFedId.cfFedId_Class*)

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary, as in the OpenAIRE Guidelined for Data Archives - see https://guidelines.openaire.eu/wiki/OpenAIRE_Guidelines:_For_Data_Archives :

* **ARK**
* **DOI**
* **Handle**
* **PURL**
* **URN**
* **URL**

Name
^^^^

(occurences: 1)

*cfResProd.cfName*

Description
^^^^^^^^^^^

(occurences: 1)

*cfResProd.cfDescr*

Languague
^^^^^^^^^

(occurences: 1)

*cfResProd.ResProd _Class*

Applicable Vocabularies
"""""""""""""""""""""""

Use ISO 639-1 (two letter codes), as recommended by CERIF.

License Types
^^^^^^^^^^^^^

(occurences: 1)

*cfResProd.ResProd_Class*

Applicable Vocabularies
"""""""""""""""""""""""

Use terms from the info:eu-repo-Access-Terms vocabulary, see http://purl.org/REP/standards/info-eu-repo#info-eu-repo-AccessRights. The allowed values are the following:

* ``info:eu-repo/semantics/closedAccess``
* ``info:eu-repo/semantics/embargoedAccess``
* ``info:eu-repo/semantics/restrictedAccess``
* ``info:eu-repo/semantics/openAccess``

If the material is licensed under a Creative Commons license then you should provide links to applicable Creative Commons licenses, e.g.: 

* http://creativecommons.org/licenses/zero/1.0/
* http://creativecommons.org/licenses/by/3.0/

Product Types (OpenAIRE)
^^^^^^^^^^^^^^^^^^^^^^^^

(occurences: 1)

*cfResProd.ResProd_Class*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary (adopted from the OpenAIRE Guidelines for Data Archives):

* **Collection**
* **Dataset**
* **Event**
* **Image**
* **Interactive Resource**
* **Model**
* **Physical Object**
* **Service**
* **Software**
* **Sound** 
* **Text**

Product Types (CERIF)
^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..1)

*cfResProd.ResProd_Class*

Applicable Vocabularies
"""""""""""""""""""""""

CERIF defines datasets at a more generic level and also comprises a range of product types:

* **Research Datasets and databases**
* **Artefact**
* **Devices and products**
* **Composition**
* **Design**
* **Software**
* **Website Content**
* **Digital or visual media**

Relationship(s) with
--------------------

Person
^^^^^^

(occurences: 0..N)

*cfResProd.cfPers_ResProd*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Creator**
* **Publisher**

as defined in CERIF Semantics  “Person Output Contributions” scheme.

Organisation
^^^^^^^^^^^^

(occurences: 0..N)

*cfResProd.cfOrgUnit_ResProd*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Creator**
* **Publisher**

as defined in CERIF Semantics “Organisation Output Contributions” scheme.

Project
^^^^^^^

(occurences: 0..N)

*cfProj.Proj_ResProd*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Originator**

as defined in CERIF Semantics “Project Output Roles” scheme. I.e. Dataset has originator Project.

(Recursive) Product / Dataset
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..N)

*cfResProd.cfResProd_ResProd*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Citation**
* **Derivation**
* **Supplement**
* **Continuation**
* **Metadata**
* **Version**
* **Part**
* **Reference**
* **Documentation**
* **Compilation**
* **Variant**
* **Identical**

Publication
^^^^^^^^^^^

(occurences: 0..N)

*cfResProd.ResPubl_ResProd*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Reference**

as defined in CERIF Semantics  “Inter-Output Relations” scheme.

Equipment
^^^^^^^^^

(occurences: 0..N)

*cfResProd.ResProd_Equip*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Generation**

as defined in CERIF Semantics “Infrastructure Output Relations” scheme.

