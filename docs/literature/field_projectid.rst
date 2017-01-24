.. _dci:fundingReference:

4. FundingReference (MA)
========================

4.1 funderName
--------------

Name of the funding provider.

4.2 funderIdentifier
--------------------

4.2.1 funderIdentifiertype
^^^^^^^^^^^^^^^^^^^^^^^^^^

4.3 awardNumber
---------------

4.3.1 awardURI
^^^^^^^^^^^^^^

4.4 awardTitle
--------------

**Usage Instruction**

.. include:: ../common/projectid.rst

**Since**

OpenAIRE Guidelines v1

**Modified**

OpenAIRE Guidelines v4

**Example**

An example utilizing all six fields:

.. code-block:: xml
   :linenos:

   <dc:relation>
     info:eu-repo/grantAgreement/EC/FP7/244909/EU/Making Capabilities Work/WorkAble
   </dc:relation>

An example for omitting the the ProjectName field (note that the number of slashes is correctly preserved):

.. code-block:: xml
   :linenos:

   <dc:relation>
     info:eu-repo/grantAgreement/EC/FP7/283595/EU//OpenAIREplus
   </dc:relation>


A correct example using the old three-part form (discouraged):

.. code-block:: xml
   :linenos:

   <dc:relation>
     info:eu-repo/grantAgreement/EC/FP7/244909
   </dc:relation>
