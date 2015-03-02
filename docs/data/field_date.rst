.. include:: ../common/replacements.rst

.. _d:date:

8. Date (M)
-----------
Different dates relevant to the work (occurrences: 0-n).

**Allowed values, examples, other constraints**

``YYYY``, ``YYYY‐MM‐DD``, ``YYYY‐MM‐DDThh:mm:ssTZD`` or any other format or level of granularity described in `W3CDTF <http://www.w3.org/TR/NOTE‐datetime>`_. Use `RKMS‐ ISO8601 <http://www.ukoln.ac.uk/metadata/dcmi/collection-RKMS-ISO8601/>`_ standard for depicting date ranges. Example: ``2004‐03‐02/2005‐06‐02``

.. note::

   *Mandatory* property in OpenAIRE instead of *recommended* in DataCite.

.. _d:datetype:

8.1 dateType (M)
~~~~~~~~~~~~~~~~

The type of date (occurrences: 1).

**Allowed values, examples, other constraints**

If Date is used, dateType is mandatory.

*Controlled List Values:*

* Accepted
* Available
* Copyrighted
* Collected
* Created
* Issued
* Submitted
* Updated
* Valid

.. note::

   Use “Issued” for the date the resource is published or distributed. To indicate the end of an embargo period, use “Available”. To indicate the start of an embargo period, use “Accepted”.

   DataCite |datacitever| further recommends use of “Created” and “Submitted”.

   Further dateTypes may be specified. Please refer to DataCite Metadata Schema |datacitever| for details.


Example
~~~~~~~

.. include:: examples/embargodate.rst
