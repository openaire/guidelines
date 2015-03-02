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

The specific content of the ``openaire_data`` set is to be determined at the local repository. OpenAIRE will **harvest all datasets** from the ``openaire_data`` set, but will **only expose datasets fulfilling at least one** of the following criteria in the OpenAIRE portal:

* The dataset is outcome of a funded research project identified by a project identifier (see section “Funding information” above).
* The dataset is linked with a publication in the OpenAIRE information space (see section “Related publications and datasets information” above).

Both criteria above may be automatically inferred by the OpenAIRE infrastructure.

Specifically a data repository may insert a dataset without funding information or link to a related publication in the ``openaire_data`` set. If later a publication harvested from a literature repository links to the dataset, the dataset will be exposed in the OpenAIRE portal. If either the literature repository or the data repository explicitly links the publication and dataset (see section ”Related publications and datasets information”), the dataset will normally be exposed in the OpenAIRE portal **within 1-2 days after harvesting** (repositories are harvested on average once a week). If the OpenAIRE infrastructure automatically has to infer the link between the publication and the dataset, it may take **up to a month after harvesting** before the dataset is exposed in the OpenAIRE portal.
