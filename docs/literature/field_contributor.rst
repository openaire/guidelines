.. _dci:contributor:

3. Contributor (R)
==================

.. _dci:contributor_contributorName:

3.1 contributorName (M)
-----------------------

3.2 givenName (O)
-----------------

3.3 familyName (O)
------------------

3.4 nameIdentifier (R)
----------------------

3.4.1 nameIdentifierScheme
^^^^^^^^^^^^^^^^^^^^^^^^^^

3.4.2 schemeURI
^^^^^^^^^^^^^^^

3.5 affiliation
---------------

3.6 contributorType
-------------------

attribute


**DCMI Definition**

An entity responsible for making contributions to the content of the resource. Examples of a Contributor include a person, an organization, or a service. Typically, the name of a Contributor should be used to indicate the entity.

**Usage Instruction**

Examples of contributors are: a supervisor, editor, technician or data collector.

Personal names should be listed as: see instructions under Creator. A “promotor”, i.e. a professor supervising a student’s work for a doctor’s degree - is considered a contributor of a dissertation in his or her role as promotor/examiner. In less-rich Unqualified DC it is difficult to express all roles in different contexts. In the PhD thesis as a document, the key figures are the author and the supervisor. In the overall PhD process other roles are involved, such as committee members and the Master of Ceremonies, but in Unqualified these roles have to be sacrificed.

In the case of organizations : see instructions under Creator The inclusion of personal and corporate name headings from authority lists constructed according to local or national thesaurus files is optional.

**Do Not Confuse With**

* :ref:`dc:publisher`
* :ref:`dci:creator`

The DC element ``contributor`` describes the scientist(s) that has/have made contributions to the given scientific output, not as a primary creator or (commercial) publisher.

**Since**

DRIVER Guidelines v2

**Example**

.. code-block:: xml
   :linenos:

   <dc:contributor>Evans, R. J.</dc:contributor>
   <dc:contributor>
     International Human Genome Sequencing Consortium
   </dc:contributor>
