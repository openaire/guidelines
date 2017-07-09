.. _dc:subject:

Subject (MA)
^^^^^^^^^^^^

DC Field
~~~~~~~~
``dc:subject``

Usage
~~~~~
*Mandatory when applicable (MA)*

Usage Instruction
~~~~~~~~~~~~~~~~~
In the DC subject element two kinds of values are possible: encode either a keyword or a classification. When both are available use separate occurrences of this element.

Use the first occurrence of the DC element ``subject`` for a human readable keyword.

In general, choose the most significant and unique words for keywords, avoiding those too general to describe a particular resource. If the subject of the resource is a person or an organization, use the same form of the name as you would if the person or organization were an author, but do not repeat the name in the ``dc:creator`` element.

For keywords/keyphrases that are not controlled by a vocabulary or thesaurus either encode multiple terms with a semi-colon separating each keyword/keyphrase; or repeat the element for each term. There are no requirements regarding the capitalization of keywords though internal (within archive) consistency is recommended.

Where terms are taken from a standard classification schema: encode each term in a separate element. Encode the complete subject descriptor according to the relevant scheme. Use the capitalisation and punctuation used in the original scheme.

It is recommended to use an URI when using classification schemes or controlled vocabularies especially when codified schemes are used DDC or UDC. Service providers can recognise encoding schemas more easy when the schema is “URI-fied” by an authority namespace. When the classification scheme is codified, use a human readable text of the code, preferably in English, directly below the codified element. For example:

.. code-block:: xml
   :linenos:

   <dc:subject>info:eu-repo/classification/ddc/641</dc:subject>
   <dc:subject>Anatomy</dc:subject>


If no specific classification scheme is used we recommend the Dewey Decimal Classification (DDC). 
More information about the DDC and the DDC Summaries can be found at https://www.oclc.org/en/dewey/resources.html . Please note that OCLC owns all copyright rights in the Dewey Decimal Classification system. Dewey, Dewey Decimal Classification, DDC, OCLC and WebDewey are registered trademarks of OCLC.

Do Not Confuse With
~~~~~~~~~~~~~~~~~~~

* :ref:`dc:type`

Since
~~~~~
DRIVER Guidelines v2

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <dc:subject>
     polar oceanography; boundary current; masstransport; water masses;
     halocline; mesoscaleeddies
   </dc:subject>
   <dc:subject>Germany--History--1933-1945</dc:subject>
   <dc:subject>info:eu-repo/classification/ddc/641</dc:subject>
   <dc:subject>Anatomy</dc:subject>
