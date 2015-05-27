.. _c:equipmententity:

8. Equipment Entity (cfEquip)
=============================

The CERIF entity cfEquipment *cfEquip* is used in the context of OpenAIRE to represent equipment/devices that are used for the generation of data sets.

Attributes
----------

Internal Identifier
^^^^^^^^^^^^^^^^^^^

(occurences: 1)

 *cfEquip.cfEquipId*

Federated Identifiers
^^^^^^^^^^^^^^^^^^^^^

(occurences: 0..N)

*cfEquip.cfFedId.cfFedId* (where the type of identifier is given through *cfEquip.cfFedId.cfFedId_Class*)

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Institution assigned unique identifier** (such as an asset inventory number) 
* **URL** (web resource giving information about the facility or equipment)

Name
^^^^

(occurences: 1)

*cfEquip.cfName*

Acronym 
^^^^^^^

(occurences: 0..1)

*cfEquip.cfAcro*

Description
^^^^^^^^^^^

(occurences: 0..1)

*cfEquip.cfDescr*

Relationship(s) with
--------------------

Dataset
^^^^^^^

(occurences: 1..N)

*cfEquip.cfResProd_Equip*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Generation**

as defined in CERIF Semantics “Infrastructure Output Relations” scheme.
