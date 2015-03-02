.. _dc:relation:

Relation (M)
^^^^^^^^^^^^

DC Field
~~~~~~~~
``dc:relation``

Usage
~~~~~
* *Mandatory*
* *Mandatory when applicable*
* *Recommended*
* *Optional*

DCMI Definition
~~~~~~~~~~~~~~~
The reference to a related resource.

Usage Instruction
~~~~~~~~~~~~~~~~~
For OpenAIRE-specific use, see sections on Project Information, Alternative Identifiers, Referenced Publications, and Referenced Datasets.

Recommended best practice is to reference the resource by means of a string or number conforming to a formal identification system. The DC element ``relation`` can be used to indicate different kinds of relations between several metadata records. If relations between metadata records are made visible by using metadata the following holds for the distinction between versions (author version and publisher version, preprint, postprint, etc.):

.. FIXME

A metadata record is self-contained Different manifestations of one and the same resource (an instance of scientific output that can be described with exactly the same bibliographic metadata, except for the DC element ``format``) are linked to one single metadata record using dc:relation.
Changes in the metadata other than the DC element ``format`` leads to creating a new metadata record of this new instance of scientific output which meets all requirements formulated in this document and has a value in the DC element ``relation``.

Do Not Confuse With
~~~~~~~~~~~~~~~~~~~

* :ref:`dc:identifier`
* :ref:`dc:source`

Since
~~~~~
DRIVER Guidelines v2

Example
~~~~~~~

Generic use:

.. code-block:: xml
   :linenos:

   <dc:relation>http://hdl.handle.net/10</dc:relation>

The value of ``dc:relation`` is the identifier of the other document.

Linking two documents:

.. code-block:: xml
   :linenos:

   <!-- Document A -->
   <dc:type>info:eu-repo/semantics/submittedVersion</dc:type>
   <dc:identifier> http://hdl.handle.net/10</dc:identifier>
   <dc:relation>http://hdl.handle.net/20</dc:relation>

.. code-block:: xml
   :linenos:

   <!-- Document B -->
   <dc:type>info:eu-repo/semantics/acceptedVersion</dc:type>
   <dc:identifier> http://hdl.handle.net/20</dc:identifier>
   <dc:relation>http://hdl.handle.net/10</dc:relation>
