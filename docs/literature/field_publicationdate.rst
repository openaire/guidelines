.. _dc:date:

10. Publication Date (M)
========================

**DCMI Definition**

A date associated with an event in the life cycle of the resource. Typically, Date will be associated with the creation or availability of the resource. Recommended best practice for encoding the date value is defined in a profile of ISO 8601 [W3CDTF] and follows the ``YYYY-MM-DD`` format.

**Usage Instruction**

The date should be formatted according to the W3C encoding rules for dates and times:

**Complete date:**

``YYYY-MM-DD`` (e.g. 1997-07-16)

where:

* ``YYYY`` [four-digit year] is ''mandatory''
* ``MM`` [two-digit month (01=January, etc.)] is ''optional''
* ``DD`` [two-digit day of month (01 through 31)] is ''optional''

**One date field – Date of Publication:**

Often repository systems have more then one date fields that serve different purposes. Date of creation, publication, modified, promotion, etc. Unqualified DC is unable to express all these dates, and for the end-user perspective it is confusing to receive more dates from the service provider. The service provider should make a choice what date- field to pick. Preferably in the end-users perspective the most logical and meaningful date will be the date of publication. To reduce the ambiguity of having a number of date fields without qualifiers, we recommend to reduce the number of fields and present the most meaningful date to the service provider. In most cases this is the date of the publication. In other cases this is the date of promotion of a PhD degree.

**No date of publication available:**

If no date of publication is available, use any other date available. It is better to use one date than no date at all.

**Datestamp additions:**

Additions like “Zulu time” should NOT be part of the metadata.

**Fuzzy dates:**

For fuzzy dates use a logical year that most represents that period, e.g. ``1650`` instead of ``17th century``.

To express more about that temporal period, one can use the ``dc:coverage`` field. A temporal period can be expressed in a standard way when precisely defined (see :ref:`dc:coverage`) or when “fuzzy” or uncertain by free text expressions. A service provider is able to sort dates based on date standards like W3CDTF. Since there is no standard for fuzzy dates for terms like “Renaissance” or “17th Century”, they will simply not appear on date-based query results.

**Since**

DRIVER Guidelines v2

**Example**

.. code-block:: xml
   :linenos:

   <dc:date>2000-12-25</dc:date>
   <dc:date>1978-02</dc:date>
   <dc:date>1650</dc:date>
