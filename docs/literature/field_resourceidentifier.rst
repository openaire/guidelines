.. _dc:identifier:

14 Resource Identifier (M)
==========================


**DCMI Definition**

An unambiguous reference to the resource within a given context.

**Usage Instruction**

Recommended best practice is to identify the resource by means of a string or number conforming to a formal identification system. Example formal identification systems include the Uniform Resource Identifier (URI), the Uniform Resource Locator (URL), the Digital Object Identifier (DOI), and the ``URN:NBN``.

The ideal use of this element is to use a direct link or a link to a jump-off page (persistent URL) from ``dc:identifier`` in the metadata record to the digital resource or a jump-off page.

Smart practice:

* use stable URL’s
* provide every identifier one can find about the publication.

  * (URL,DOI,URN:NBN,ISBN,ISSN,etc.)

* place the “most appropriate” identifier in the form of a URL at the top of the list of Identifiers. In almost all cases this is the one that will be used by a service provider to let an end-user refer to. This can be a link to a jump-off page or a direct link to the file. Also this can be a direct URL, or a redirection URL, like PURL, HANDLE or other international resolution mechanisms.

**Do Not Confuse With**

* :ref:`dc:relation` (Use ``dc:relation`` to refer from one version of the resource to another.)
* :ref:`dc:source` (Use ``dc:source`` for bibliographic citation of the originating resource.)

**Since**

DRIVER Guidelines v2

**Example**

In this example the identifiers are sorted so that URLs are given first. The first URL will be considered as “most appropriate” and will be used in e.g. OpenAIRE to let an end-user redirect to. In this case the handle redirects to the jump-off page. A jump-off page is a good way to refer to. The end-user has the opportunity to see more information about the object(s) he has found, see the context and enjoy the other services a local repository has to offer:

.. code-block:: xml
   :linenos:

   <dc:identifier>http://hdl.handle.net/1234/5628 </dc:identifier>
   <dc:identifier>http://arno.unimaas.nl/show.cgi?fid=5628 </dc:identifier>
   <dc:identifier>http://n2t.info/urn:nbn:nl:ui:14123456789</dc:identifier>
   <dc:identifier>urn:nbn:nl:ui:13-123456789</dc:identifier>
   <dc:identifier>urn:isbn:123456789</dc:identifier>
   <dc:identifier>info:doi:10-123456789</dc:identifier>
