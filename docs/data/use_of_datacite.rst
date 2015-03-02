Use of DataCite
===============
OpenAIRE has adopted the DataCite Metadata Schema as the basis for harvesting and importing metadata about datasets from data archives.

The core mission of DataCite is to build and maintain a sustainable framework that makes it possible to cite data through the use of persistent identifiers, DOIs.

OpenAIRE shares the goal of the DataCite Metadata Schema - to provide a domain agnostic metadata schema and provide interoperability through a small number of properties - making interoperability possible in the simplest manner possible and as a result keep the technical barriers for implementation as low as possible.

We would like to thank DataCite for their kind support and help making these OpenAIRE Guidelines for Data Archive Managers possible.

What's different
^^^^^^^^^^^^^^^^
In this document you will find the needed properties to make your data archive compatible with the OpenAIRE infrastructure. OpenAIRE has adopted the DataCite Metadata Schema version 3.0 with some minor adjustments.

- OpenAIRE accepts other persistent identifier schemes and not only a DOI in :ref:`d:identifiertype`.
- OpenAIRE recommends exporting links to related publications and datasets (i.e. :ref:`d:relatedidentifier` property and attributes are *mandatory when applicable*).
- OpenAIRE recommends using the :ref:`d:contributor` property to relate a dataset to funding information.
- DataCite optional properties :ref:`d:date` and :ref:`d:description` are *mandatory* in OpenAIRE.
- OpenAIRE enforces an encoding scheme on DataCite property :ref:`d:rights`.

.. _accessrights:

Access rights and license information
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
OpenAIRE uses the access rights to enable a better user experience by declaring the access rights clear and explicit in the portal. Access rights are specified using the :ref:`d:rights` property. Please see example of encoding scheme in the section above.

.. include:: examples/accessright.rst

.. _fundinginfo:

Funding information
^^^^^^^^^^^^^^^^^^^
OpenAIRE have a specific use of the :ref:`d:contributor` property to identify links to funding steams.

One of OpenAIRE’s main goals is to link research output to (EC) research funding. The following application of the contributor property allows unique and persistent identification of the funder who has funded wholly or partly the dataset described.

The following properties are mandatory when applicable to provide funding information: :ref:`d:contributor`, :ref:`d:contributortype`, :ref:`d:contributorname`, :ref:`d:contributor_nameidentifier` and :ref:`d:contributor_nameidentifierscheme`.

An example for linking a research output to the OpenAIREplus FP7 project:

.. include:: examples/funding.rst


.. _relations:

Related publications and datasets information
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
OpenAIRE **harvests all datasets** from a data repository, but **exposes** only certain datasets in the OpenAIRE portal. See the :ref:`d:setcontent` for specific details of which datasets are exposed.

For example, datasets related to publication will be exposed in the OpenAIRE portal. The link between the dataset and publication may be explicit defined, as described in this section, or automatically inferred by the OpenAIRE infrastructure.

If the link is explicit defined, the dataset will be exposed in the OpenAIRE portal **within 1-2 days after harvesting** (a repository is harvested once a week on average). If the link is automatically inferred by the OpenAIRE infrastructure it may take **up to a month after harvesting** before the dataset is exposed in the OpenAIRE portal. It is thus *mandatory when applicable* to provide links to related publications and datasets when these links are available in the repository, and thereby ensure faster exposure of the dataset in the OpenAIRE portal.

Related identifiers
~~~~~~~~~~~~~~~~~~~
DataCite Metadata Schema allows linking publications and datasets by use of persistent identifiers to uniquely identify the resource being described (A) typically a dataset but not limited to that, and the related resource (B) in the case of OpenAIRE typically a publication or a dataset.

Related publications/datasets must have the following properties: :ref:`d:relatedidentifier`, :ref:`d:relatedidentifiertype` and :ref:`d:relationtype`.

.. include:: examples/relatedidentifier.rst

.. _d:embargodate:

Embargo date information
^^^^^^^^^^^^^^^^^^^^^^^^
For OpenAIRE two main types of dates are relevant. When the data were made available, published or uploaded to a formal database, this is the date the data were ''Issued''.

Sometimes data may be embargoed for a period; this information should be managed by the data provider and expressed by exporting an ''Available'' date to indicate the end of an embargo period and an ''Accepted'' date to indicate the start of an embargo period.

.. include:: examples/embargodate.rst
