.. _d:subject:

6. Subject (R)
--------------
Subject, keyword, classification code, or key phrase describing the resource (occurrences: 0-n).

**Allowed values, examples, other constraints**

Free text.

.. _d:subjectscheme:

6.1 subjectScheme (O)
~~~~~~~~~~~~~~~~~~~~~
The name of the subject scheme or classification code or authority if one is used (occurrences: 01).

**Allowed values, examples, other constraints**

Free text.

.. _d:subject_schemeuri:

6.2 schemeURI (O)
~~~~~~~~~~~~~~~~~
The URI of the subject identifier scheme (occurrences: 0-1).

**Allowed values, examples, other constraints**

Examples:

* http://id.loc.gov/authorities/subjects
* http://dewey.info/

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <subjects>
    <subject>Earth sciences and geology</subject>
    <subject subjectScheme="DDC" schemeURI="http://dewey.info/">
    551 Geology, hydrology, meteorology
    </subject>
   </subjects>
