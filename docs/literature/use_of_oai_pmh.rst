Use of OAI-PMH
==============

OpenAIRE uses the `OAI-PMH v2.0 protocol <http://www.openarchives.org/OAI/openarchivesprotocol.html>`_ for harvesting publication metadata.

Metadata Format
^^^^^^^^^^^^^^^
OpenAIRE expects metadata to be encoded in the
`Dublin Core <http://dublincore.org/documents/dces/>`_ metadata format (metadataPrefix
``oai_dc``). For information on how to use the individual DC fields, please refer
to the section "Use of OAI-DC" below.

OpenAIRE OAI Set
~~~~~~~~~~~~~~~~
For harvesting the records relevant to OpenAIRE, the use of a specific `OAI-Set <http://www.openarchives.org/OAI/openarchivesprotocol.html#Set>`_ at the local repository is *mandatory*. The set must have the following characteristics:

.. FIXME

======== ============
setName  setSpec
======== ============
OpenAIRE ``openaire``
======== ============

.. note::
   A harvester only uses the **setSpec** value to perform selective harvesting. The letters of the setSpec must be in lowercase.

Set content
~~~~~~~~~~~

Publications to be inserted in the OpenAIRE set must conform to **at least one**
of the following criteria:

* They are available in Open Access (full text with no access restrictions)
* They are the outcome of a funded research project identified by a project identifier (see below) regardless of their access status (see section below on [[Literature Guidelines: Metadata Field Access Level|Application Profile Field Access Level]]).

.. FIXME

Compatibility of aggregators
^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Besides individual repositories and journals, also aggregators (e.g., on the national level) can become OpenAIRE compatible. In this case, additional provenance information on the original content providers harvested by the aggregator has to be encoded for OpenAIRE.
In accordance with the `OAI-PMH guidelines <http://www.openarchives.org/OAI/2.0/guidelines-provenance.htm>`_, the provenance information has to be provided in the ``about`` element of an OAI record, as displayed in the following example:

.. code-block:: xml
   :linenos:

    <about>
      <provenance xmlns="http://www.openarchives.org/OAI/2.0/provenance"
      xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
      xsi:schemaLocation="http://www.openarchives.org/OAI/2.0/provenance
      http://www.openarchives.org/OAI/2.0/provenance.xsd">
        <originDescription altered="true" harvestDate="2012-09-17T14:58:36Z">
          <baseURL>http://dspace.library.uu.nl:8080/dspace-oai/request</baseURL>
          <identifier>oai:dspace.library.uu.nl:1874/218065</identifier>
          <datestamp>2012-01-19T12:38:56Z</datestamp>
          <metadataNamespace>
            http://www.openarchives.org/OAI/2.0/oai_dc/
          </metadataNamespace>
        </originDescription>
      </provenance>
    </about>

.. note::
   It is recommended to consider the section `Compatibility of Aggregators <https://openaire-guidelines-for-literature-repository-managers.readthedocs.io/en/latest/use_of_oai_pmh.html#compatibility-of-aggregators>`_
   under `OpenAIRE Guidelines for Institutional and Thematic Repository Managers v4 <https://openaire-guidelines-for-literature-repository-managers.readthedocs.io/en/latest/>`_ as well.
