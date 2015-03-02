.. _dc:relation_datasetreference:

Dataset Reference (R)
^^^^^^^^^^^^^^^^^^^^^

DC Field
~~~~~~~~
``dc:relation``

Usage
~~~~~
*Recommended*

Usage Instruction
~~~~~~~~~~~~~~~~~

Encodes links to research datasets connected with this publication. The syntax of info:eu-repo/semantics/dataset is: ``info:eu-repo/semantics/dataset/<scheme>/<identifier>`` where ``<scheme>`` must be one of the following:

* ``ark`` – Archival Resource Key
* ``doi`` – Digital Object Identifier
* ``hdl`` – Handle
* ``purl`` – Persistent Uniform Resource Locator
* ``url`` – Uniform Resource Locator
* ``urn`` – Uniform Resource Name

Since
~~~~~
OpenAIRE Guidelines v3

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <dc:relation>
     info:eu-repo/semantics/dataset/doi/10.1234/789.1
   </dc:relation>
