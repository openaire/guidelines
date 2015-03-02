.. _d:title:

3. Title (M)
------------
A name or title by which a resource is known (occurrences: 1-n).

**Allowed values, examples, other constraints**

Free text.

.. _d:titletype:

3. titleType (O)
~~~~~~~~~~~~~~~~
The type of Title (occurrences: 0-1).

**Allowed values, examples, other constraints**

*Controlled List Values:*

* Alternative Title
* Subtitle
* TranslatedTitle

Example
^^^^^^^
.. code-block:: xml
   :linenos:

   <titles>
    <title>
     National Institute for Environmental Studies and Center
     for Climate System Research Japan
    </title>
    <title titleType="Subtitle">A survey</title>
   </titles>
