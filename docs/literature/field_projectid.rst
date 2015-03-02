.. _dc:relation_projectid:

Project Identifier (MA)
^^^^^^^^^^^^^^^^^^^^^^^

DC Field
~~~~~~~~
``dc:relation``

Usage
~~~~~
*Mandatory when applicable*

Usage Instruction
~~~~~~~~~~~~~~~~~

.. include:: ../common/projectid.rst

Since
~~~~~
OpenAIRE Guidelines v1


Example
~~~~~~~

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
