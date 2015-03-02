.. _dc:relation_publicationreference:

Publication Reference (R)
^^^^^^^^^^^^^^^^^^^^^^^^^

DC Field
~~~~~~~~
``dc:relation``

Usage
~~~~~
*Recommended*

Usage Instruction
~~~~~~~~~~~~~~~~~
Encode links to publications referenced by this publication. The syntax is: ``info:eu-repo/semantics/reference/<scheme>/<identifier>`` where ``<scheme>`` must be one of the following:

* ``ark`` – Archival Resource Key
* ``arxiv`` – arXiv.org identifier
* ``doi`` – Digital Object Identifier
* ``hdl`` – Handle
* ``isbn`` – International Standard Book Number
* ``issn`` – International Standard Serial Number
* ``pmid`` – PubMed ID
* ``purl`` – Persistent Uniform Resource Locator
* ``url`` – Uniform Resource Locator
* ``urn`` – Uniform Resource Name
* ``wos`` – Web of Science accession number

Since
~~~~~
OpenAIRE Guidelines v3

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <dc:relation>
     info:eu-repo/semantics/reference/doi/10.1234/789.1
   </dc:relation>
