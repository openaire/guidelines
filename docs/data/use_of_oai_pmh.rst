.. _d:oaipmh:

Use of OAI-PMH
===============
OpenAIRE uses the OAI-PMH v2.0 protocol for harvesting dataset metadata.

.. _d:metadataformat:

Metadata Format
^^^^^^^^^^^^^^^
OpenAIRE expects metadata to be encoded in the DataCite metadata format (metadataPrefix ``oai_datacite``) . For information on how to use the individual DataCite properties, please refer to :ref:`d:applicationprofile`.

.. _d:oaiset:

OpenAIRE OAI Set
^^^^^^^^^^^^^^^^
A specific OAI-Set at the local repository should be configured to select records relevant to OpenAIRE for harvesting. The following characteristics of the set are *recommended*:

======== =================
setName  setSpec
======== =================
OpenAIRE ``openaire_data``
======== =================

.. note::
   A harvester only uses the **setSpec** value to perform selective harvesting. The letters of the setSpec must be in small caps.

.. _d:setcontent:

Set content
^^^^^^^^^^^

The specific content of the ``openaire_data`` set is to be determined at the local repository. OpenAIRE will **harvest all datasets** from the ``openaire_data`` set.
