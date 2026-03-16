.. _dc:creator:

Creator (M)
^^^^^^^^^^^

DC Field
~~~~~~~~
``dc:creator``

Usage
~~~~~
*Mandatory*

Usage Instruction
~~~~~~~~~~~~~~~~~
Examples of a Creator include a person, an organization, or a service. If necessary, repeat this element for multiple authors.

Use inverted name, so the syntax will be the following: “surname”, “initials” (“first name”) “prefix”. For example Jan Hubert de Smit becomes

.. code-block:: xml

   <dc:creator>Smit, J.H. (John) de</dc:creator>

Within the scope of unqualified DC it is recommended to use a standardised writing style for names, use the writing style used by the publisher when this is available. When that is not available use the encoding of the APA bibliographic writing style as in a reference list when applicable. (outside the scope of Unqualified DC more precise and granular formatting methods are available.)

When initials and first name are both available use this formatting:

.. code-block:: xml

   <dc:creator>Janssen, J. (John)</dc:creator>

Generational suffixes (Jr., Sr., etc.) should follow the surname. When in doubt, give the name as it appears, and do not invert. Omit titles (like “Dr”). For example: “Dr. John H. de Smit Jr.” becomes

.. code-block:: xml

   <dc:creator>Smit Jr., J.H. (John) de</dc:creator>
   
ORCID-IDs should be added as a URL, separted from the name by a semicolon. 

.. code-block:: xml

   <dc:creator>Evans, R.J. ; https://orcid.org/1234-1234-1234-1234</dc:creator>

In the case of an organization name which clearly includes an organizational hierarchy, list the parts of the hierarchy from largest to smallest, separated by full stops.

For example:

.. code-block:: xml

   <dc:creator>Utrecht University. Department of Computer Sciences</dc:creator>

If it is not clear whether there is a hierarchy present, or unclear which is the larger or smaller portion of the body, give the name as it appears in the resource. Only encode organisations in this element to indicate corporate authorship, not to indicate the affiliation of an individual.

The inclusion of personal and corporate name headings from authority lists constructed according to local or national thesaurus files is optional.

It is recommended to encode thesauri with an URI, for service providers to recognise the thesaurus schema. For example:

.. code-block:: xml

   <dc:creator>urn:NationalOrgThesaurus:nl/234</dc:creator>

In cases of lesser responsibility, other than authorship, use ``dc:contributor``. If the nature of the responsibility is ambiguous, recommended best practice is to use ``dc:publisher`` for organizations, and ``dc:creator`` for individuals.


Do Not Confuse With
~~~~~~~~~~~~~~~~~~~
* :ref:`dc:contributor`
* :ref:`dc:publisher`

Since
~~~~~

DRIVER Guidelines v2

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <dc:creator>Evans, R.J.</dc:creator>
   <dc:creator>Evans, R.J. ; https://orcid.org/1234-1234-1234-1234</dc:creator>
   <dc:creator>Walker Jnr., John</dc:creator>
   <dc:creator>
     International Human Genome Sequencing Consortium
   </dc:creator>
   <dc:creator>
     Loughborough University. Department of Computer Science
   </dc:creator>
