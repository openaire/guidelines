.. _dci:alternativeidentfier:

5. AlternateIdentifier (R)
==========================

An identifier or identifiers other than the primary Identifier applied to the resource being registered. This may be any alphanumeric string which is unique within its domain of issue. May be used for local identifiers. AlternateIdentifier should be used for another identifier of the same instance (same location, same file).

5.1 alternateIdentifierType (O)
-------------------------------


**Usage Instruction**

List alternative identifiers for this publication that are not the primary identifier (repository splash page), e.g., the DOI of publisher’s version, the PubMed/arXiv ID. The term is defined by ``info:eu-repo/semantics/altIdentifier/<scheme>/<identifier>`` where ``<scheme>`` must be one of the following:

* ``ark`` – Archival Resource Key
* ``arxiv`` – arXiv.org identifier
* ``doi`` – Digital Object Identifier
* ``hdl`` – Handle
* ``isbn`` – International Standard Book Number
* ``pissn`` – International Standard Serial Number (print version)
* ``eissn`` – International Standard Serial Number (electronic Version)
* ``pmid`` – PubMed ID
* ``purl`` – Persistent Uniform Resource Locator
* ``urn`` – Uniform Resource Name
* ``wos`` – Web of Science accession number

**Since**

OpenAIRE Guidelines v3

**Example**

.. code-block:: xml
   :linenos:

   <dc:relation>
     info:eu-repo/semantics/altIdentifier/doi/10.1234/789.1
   </dc:relation>
