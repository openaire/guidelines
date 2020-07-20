.. _d:resourcetype:

10. ResourceType (R)
--------------------
A description of the resource (occurrences: 0-1).

**Allowed values, examples, other constraints**

The format is open, but the preferred format is a single term of some detail so that a pair can be formed with the sub-property.

Text formats can be free-text OR terms from the `CASRAI Publications resource type list <https://web.archive.org/web/20150221150902/http://dictionary.casrai.org/research-personnel-profile/contributions/outputs/publications>`_.

Examples:

``Dataset/Census Data``, where ``Dataset`` is resourceTypeGeneral value and ``Census Data`` is ResourceType value.
``Text/Conference Abstract``, where ``Text`` is ResourceTypeGeneral value and ``Conference Abstract`` is resourceType value aligned with CASRAI Publications term.

.. _d:resourcetypegeneral:

10.1 resourceTypeGeneral (R)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~
The general type of a resource (occurrences: 1).

**Allowed values, examples, other constraints**

If ResourceType is used, resourceTypeGeneral is mandatory.

*Controlled List Values:*

* Audiovisual
* Collection
* Dataset
* Event
* Image
* InteractiveResource
* Model
* PhysicalObject
* Service
* Software
* Sound
* Text
* Workflow
* Other

Combine “Text” with free-text or terms from the CASRAI Publications resource type list found `here <https://web.archive.org/web/20150221150902/http://dictionary.casrai.org/research-personnel-profile/contributions/outputs/publications>`_.

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <resourceType resourceTypeGeneral="Image">Animation</resourceType>
