.. _dc:publisher:

9. Publisher (MA)
=================

**DCMI Definition**

An entity responsible for making the resource available. Examples of a Publisher include a person, an organization, or a service. Typically, the name of a Publisher should be used to indicate the entity.

**Usage Instruction**

The (commercial or non-commercial) publisher of the resource; not the (sub)institution the author is affiliated with. Publisher is used only in the bibliographic / functional sense, not an organisational one. Use only the full name of the given (commercial) publisher, not the name of an organization or institute that is otherwise [in a broader sense] associated with the creator.

With university publications place the name of the faculty and/or research group or research school after the name of the university. In the case of organizations where there is clearly a hierarchy present, list the parts of the hierarchy from largest to smallest, separated by full stops. If it is not clear whether there is a hierarchy present, or unclear which is the larger or smaller portion of the body, give the name as it appears in the eprint.

The use of publisher names from authority lists constructed according to local or national thesaurus files is optional.

**Do Not Confuse With**

* :ref:`dci:contributor`
* :ref:`dci:creator`

In most cases the publisher and the creator are not the same.

**Since**

DRIVER Guidelines v2

**Example**

.. code-block:: xml
   :linenos:

   <dc:publisher>
     Loughborough University. Department of Computer Science
   </dc:publisher>
   <dc:publisher>John Wiley &amp; Sons, Inc. (US)</dc:publisher>
