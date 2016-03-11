.. _c:electronicaddressentity:

9. Electronic Address Entity (cfEAddr)
======================================

The CERIF entity cfElectronicAddress *cfEAddr* is used in the context of OpenAIRE to represent electronic addresses of persons and organisations.

Attributes
----------

Internal Identifier
^^^^^^^^^^^^^^^^^^^

(occurences: 1)

*cfEAddr.cfEAddrId*

URI
^^^

(occurences: 1)

*cfEAddr.cfURI*

Relationship with
--------------------

Person 
^^^^^^

(occurences: 1..N)

*cfEAddr.cfPers_EAddr*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Email**
* **Fax**
* **Phone**

as defined in CERIF Semantics “Person Contact Details” scheme.
