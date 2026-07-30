.. _dc:rights_accesslevel:

Access Level (M)
^^^^^^^^^^^^^^^^

DC Field
~~~~~~~~
``dc:rights``

Usage
~~~~~
*Mandatory*

Usage Instruction
~~~~~~~~~~~~~~~~~

Use terms from the `COAR Access Right Vocabulary`_ <https://vocabularies.coar-repositories.org/access_rights/>`_ . The values are:

======================================== ========================
values                                   label
======================================== ========================
http://purl.org/coar/access_right/c_abf2 ``open access``
http://purl.org/coar/access_right/c_f1cf ``embargoed access``
http://purl.org/coar/access_right/c_16ec ``restricted access``
http://purl.org/coar/access_right/c_14cb ``metadata only access``
======================================== ========================

Example
~~~~~~~
.. code-block:: xml
   :linenos:

   <dc:rights>http://purl.org/coar/access_right/c_abf2</dc:rights>
