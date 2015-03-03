.. include:: ../common/replacements.rst

.. _d:applicationprofile:

Application Profile
-------------------
OpenAIRE builds on the DataCite Metadata Schema |datacitever| by making some of the otherwise optional DataCite properties mandatory, as well as enforcing specific encoding schemes on the values of some DataCite properties. The table below details the differences from the DataCite Metadata Schema.

.. include:: ../common/definitions.rst

The recommended status is made primarily to encourage users to input certain properties when creating a metadata record to enhance services.

.. important::

   The table below details only differences from the DataCite Metadata Schema |datacitever|. Please refer to the DataCite Metadata Schema |datacitever| for definition of properties and their encoding schemes: |datacitelink|.


.. csv-table::
   :header: "Property", "Comment"
   :file: tables/application_profile.csv
   :widths: 30, 70


.. toctree::
   :maxdepth: 1
   :hidden:

   field_identifier
   field_creator
   field_title
   field_publisher
   field_publicationyear
   field_subject
   field_contributor
   field_date
   field_language
   field_resourcetype
   field_alternateidentifier
   field_relatedidentifier
   field_size
   field_format
   field_version
   field_rights
   field_description
   field_geolocation
