.. _dc:type:

11. Publication Type (M)
========================

**Usage**

Publication type is used for the following purposes:

* **Mandatory (M)**: Publication type (controlled): to indicate the type of publication based on the `info:eu-repo-publication-type-terms <https://wiki.surfnet.nl/display/standards/info-eu-repo/#info-eu-repo-Publicationtypes>`_ vocabulary.
* **Optional (O)**: Publication type (free): to indicate the type of publication based on a local repository vocabulary.

**DCMI Definition**

The type of scientific output the resource is a manifestation of. In the DC element type the kind of dissemination, or the intellectual and/or content type of the resource is described. It is used to explain to the user what kind of resource he is looking at. Is it a book or an article. Was it written for internal or external use, etc.

**Usage Instruction**

**Publication types (controlled):**

The first occurrence of the DC Element ``type`` is mandatory and should be used for the type indication of the scientific output based on the ``info:eu-repo`` publication type vocabulary:

* ``info:eu-repo/semantics/article``
* ``info:eu-repo/semantics/bachelorThesis``
* ``info:eu-repo/semantics/masterThesis``
* ``info:eu-repo/semantics/doctoralThesis``
* ``info:eu-repo/semantics/book``
* ``info:eu-repo/semantics/bookPart``
* ``info:eu-repo/semantics/review``
* ``info:eu-repo/semantics/conferenceObject``
* ``info:eu-repo/semantics/lecture``
* ``info:eu-repo/semantics/workingPaper``
* ``info:eu-repo/semantics/preprint``
* ``info:eu-repo/semantics/report``
* ``info:eu-repo/semantics/annotation``
* ``info:eu-repo/semantics/contributionToPeriodical``
* ``info:eu-repo/semantics/patent``
* ``info:eu-repo/semantics/other``

**Publication types (free text):**

The second occurrence of the DC Element ``type`` is optional and should be used for the subtype indication of the scientific output.

**Do Not Confuse With**

* :ref:`dc:format`

DC element `type` describes the kind of academic output the resource is a representation of. DC element ‘format’ describes the media type of this resource.

**Since**

DRIVER Guidelines v2

**Example**

.. code-block:: xml
   :linenos:

   <dc:type>info:eu-repo/semantics/article</dc:type>
