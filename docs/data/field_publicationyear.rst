.. _d:publicationyear:

5. PublicationYear (M)
----------------------
The year when the data was or will be made publicly available. (occurrences: 1)

**Allowed values, examples, other constraints**

Year in the form: ``YYYY``

If an embargo period has been in effect, use the date when the embargo period ends.

In the case of datasets, "publish" is understood to mean making the data available on a specific date to the community of researchers.

If there is no standard publication year value, use the date that would be preferred from a citation perspective.

.. note::

   See :ref:`d:date` and :ref:`d:datetype` for the recommended application of embargo period in OpenAIRE.

Additional guidance
~~~~~~~~~~~~~~~~~~~

The year when the data was or will be made publicly available. In the case of datasets, "publish" is understood to mean making the data available on a specific date to the community of researchers.

* If that date cannot be determined, use the date of registration.
* If an embargo period has been in effect, use the date when the embargo period ends.
* If there is no standard publication year value, use the date that would be preferred from a citation perspective.

*In the case of a digitized version of a physical object*

If the DOI is being used to identify a digitised version of an original item, the recommended approach is to supply the :ref:`d:publicationyear` for the digital version and not the original object.

The :ref:`d:title` field may be used to convey the approximate or known date of the original object. Other metadata properties available for additional date information about the object include: :ref:`d:subject` and :ref:`d:description`. However, only :ref:`d:title` will be part of the citation.

If the DOI is being used to identify the original object and the publication date of this is unknown or not standard then we recommend the following:

* Use the date that would be preferred from a citation perspective.

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <publicationYear>2004</publicationYear>
