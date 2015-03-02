.. _d:description:

17. Description (MA)
--------------------
All additional information that does not fit in any of the other categories. May be used for technical information (occurrences: 0-n).

**Allowed values, examples, other constraints**

The format is open.

It is a best practice to supply a description.

.. note::

   *Mandatory when applicable* property in OpenAIRE instead of optional in DataCite.

.. _d:descriptiontype:

17.1 descriptionType (MA)
~~~~~~~~~~~~~~~~~~~~~~~~~

The type of the Description. (occurrences: 1).

**Allowed values, examples, other constraints**

If Description is used, descriptionType is mandatory.

*Controlled List Values:*

* Abstract
* Methods
* SeriesInformation
* TableOfContents
* Other

.. note::

   Use of "Abstract" is *mandatory when applicable* in OpenAIRE instead of *recommended* in DataCite.

Example
~~~~~~~
.. code-block:: xml
   :linenos:


   <descriptions>
      <description descriptionType="Abstract">
        This is an abstract
      </description>
      <description descriptionType="Other">
        This is e.g. a note.
      </description>
   </descriptions>
