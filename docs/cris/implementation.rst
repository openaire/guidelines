Technical Implementation Guidelines
-----------------------------------

Data representation in CERIF XML
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The CERIF XML style allowed is the one defined in CERIF 1.6 XML specification. The following rules apply – however we refer to the full specification for the details [#f1]_ :

#. The CERIF data must be represented as descendants of a root XML element, “CERIF”.
#. Direct descendants of the CERIF elements must be only simple CERIF Entities [#f2]_ (such as Person; Project; OrganisationUnit; ResultPublication; ResultProduct) not multi-lingual or link entities or federated identifiers. The list of CERIF Research Entities relevant to OpenAIREplus is the following:

    cfProject (cfProj)

    cfPerson (cfPers)

    cfOrganisationUnit (cfOrgUnit)

    cfResultPublication (cfResPubl)

    cfResultProduct (cfResProd)

    cfFunding (cfFund)

    cfService (cfSrv)

    cfEquipment (cfEquip)

    cfElectronicAddress (cfEAddr)

#. Each CERIF Research Entity in the CERIF XML file embeds multilingual attributes, link entities and federated identifiers. CERIF Research Entities themselves must not be embedded within another CERIF entity; they can be direct descendants of exclusively the root CERIF XML element. Only links to other entities are allowed to be embedded into CERIF Research entities. 
#. Link entities must appear at both ends of a relationship. For example, if cfProject A is related to cfOrgUnit B, the linked entity cfProj_OrgUnit must appear embedded in the XML record of both cfProject A and cfOrgUnit B. Therefore, the XML element of every CERIF Research Entity instance must embed link entities for all the relationships to which the entity instance participates. 
#. Each link entity contains, among others, the identifiers of a classification (term) that denotes the semantics of the relationship and the classification scheme (vocabulary) to whom the term belongs; neither the detailed specification of the classification nor detailed specification of the classification scheme. Every classification and classification scheme used in link entities should belong to the set of classifications and classification schemes that constitute the OpenAIRE CERIF Semantics specification (see Appendix X). Therefore, every identifier used for specifying semantics of link entities in the CERIF XML exposed by CRIS systems should be among the identifiers (UUIDs) contained in the OpenAIRE CERIF Semantics specification.
#. Referential integrity constraints for all relationships among entities should be satisfied in the CERIF XML data provided by the CRIS system. Therefore, it is required that all CERIF objects referenced in the linking relationships in the CERIF XML data are actually represented in the data provided by the same CRIS system. For example, consider the case of a relationship between cfOrgUnit A and cfProject B that is included in the source CRIS system. To accomplish this, the CERIF XML data exported by the CRIS system must contain:

    a. An XML record for cfOrgUnit A. This XML record must contain, as a nested XML element, the link entity cfProj_OrgUnit.

    b. An XML record for cfProj B. This XML record must contain, as a nested XML element, the link entity cfProj_OrgUnit.

   It is worth noting that the two aforementioned XML records may be contained in distinct sets of XML records exported by the CRIS system through separate OAI-PMH sets (see Section “OpenAIRE OAI-PMH Set”).

.. rubric:: Footnotes

.. [#f1] CERIF 1.6 XML Specification
.. [#f2] CERIF 1.6 XML: http://www.eurocris.org/Index.php?page=CERIF-1.6&t=1

CERIF Semantic Layer link entities implementation in OpenAIRE CERIF XML
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The applicable vocabularies will be provided and thus recognised by the OpenAIRE infrastructure via identifiers (UUIDs) in the CERIF cfClass.cfClassId attributes’ values. Those specific vocabularies that must be used by CRIS systems harvested by OpenAIRE are specified in the tables of the section entitled “CRIS information elements relevant for OpenAIRE”.

For the specific case of external vocabularies utilised by the OpenAIRE guidelines (ISO 3166-1 for countries, ISO 639-1 for languages and NUTS for geographical regions) the cfClass.cfClassId attributes’ values will contain the codes of the terms in the respective standard (e.g. “GB” for United Kingdom in ISO-3166-1), while the cfClass.cfClassTerm.cfTerm values will be the human readable labels of the corresponding value (e.g. “United  Kingdom (the)” for the United Kingdom in ISO-3166-1). UUIDs will not be used as cfClassId values for these external vocabularies. The associated CERIF semantics file gives just a few example entries.

OAI-PMH for Harvesting
^^^^^^^^^^^^^^^^^^^^^^

OpenAIRE uses the OAI-PMH v2.0 protocol for harvesting metadata from CRIS systems.

Metadata Format
"""""""""""""""

OpenAIRE expects metadata from CRIS systems to be encoded in the CERIF XML metadata format, as specialised for OpenAIRE. The following metadata prefix should be used: oai_cerif_openaire. For information on how to use the OpenAIRE CERIF XML please refer to the CERIF XML specification and the specialisations of CERIF XML defined in the present document.

OpenAIRE OAI-PMH Sets
"""""""""""""""""""""

For harvesting the records relevant to OpenAIRE, the use of specific OAI-PMH sets at the local CRIS system is mandatory. The description and required characteristics of the sets are provided in the following table:

+---------------------------------------------------------+-----------------------------------------+
|Description                                              |Required characteristics                 |
+=========================================================+=========================================+
| | The entire graph of CERIF entities in the source      | | **setName:** OpenAIRE_CRIS            |
| | CRIS system of relevance to OpenAIRE. CERIF XML       | | **setSpec:** openaire_cris            |
| | records for all vocabularies (classification schemes) |                                         |
| | and terms (classifications) used may be omitted,      |                                         |
| | since they should be a subset of what is being        |                                         |
| | specified in the OpenAIRE CERIF Semantics             |                                         |
| | specification.                                        |                                         |
+---------------------------------------------------------+-----------------------------------------+
| | The list of CERIF XML records for persons with        | | **setName:** OpenAIRE_CRIS_persons    |
| | embedded multi-lingual entities, federated identifiers| | **setSpec:** openaire_cris_persons    |
| | and link entities and for associated electronic       |                                         |
| | addresses.                                            |                                         |
+---------------------------------------------------------+-----------------------------------------+
| | The list of CERIF XML records for projects with       | | **setName:** OpenAIRE_CRIS_projects   |
| | embedded multi-lingual entities, federated identifiers| | **setSpec:** openaire_cris_projects   |
| | and link entities.                                    |                                         |
+---------------------------------------------------------+-----------------------------------------+
| | The list of CERIF XML records for organisation units  | | **setName:** OpenAIRE_CRIS_orgunits   |
| | with embedded multi-lingual entities, federated       | | **setSpec:** openaire_cris_orgunits   |
| | identifiers and link entities.                        |                                         |
+---------------------------------------------------------+-----------------------------------------+
| | The list of CERIF XML records for funding with        | | **setName:** OpenAIRE_CRIS_funding    |
| | embedded multi-lingual entities, federated identifiers| | **setSpec:** openaire_cris_funding    |
| | and link entities.                                    |                                         |
+---------------------------------------------------------+-----------------------------------------+
| | The list of CERIF XML records for publications with   || **setName:** OpenAIRE_CRIS_publications|
| | embedded multi-lingual entities, federated identifiers|| **setSpec:** openaire_cris_publications|
| | and link entities.                                    |                                         |
+---------------------------------------------------------+-----------------------------------------+
|| The list of CERIF XML records for datasets with        || **setName:** OpenAIRE_CRIS_datasets    |
|| embedded multi-lingual entities, federated identifiers || **setSpec:** openaire_cris_datasets    |
|| and link entities and for associated equipment.        |                                         |
+---------------------------------------------------------+-----------------------------------------+
|| The list of CERIF XML records for services with        || **setName:** OpenAIRE_CRIS_services    |
|| embedded multi-lingual entities, federated identifiers || **setSpec:** openaire_cris_services    |
|| and link entities.                                     |                                         |
+---------------------------------------------------------+-----------------------------------------+

Referential integrity constraints for all relationships among entities should be satisfied in the CERIF XML data provided by the CRIS system, as mentioned in the “Data representation in CERIF XML” sub-section above. This holds also for the case that entity instances related via link entities are retrieved through different OAI-PMH sets. For example, consider the case of a relationship between cfOrgUnit A and cfProject B that is included in the source CRIS system. To accomplish this, the CERIF XML data exported by the CRIS system must contain:

a. An XML record for cfOrgUnit A. This XML record must contain, as a nested XML element, the link entity cfProj_OrgUnit. The XML record of cfOrgUnit A must be available through both sets **openaire_cris** and **openaire_cris_orgunits**.

b. An XML record for cfProj B. This XML record must contain, as a nested XML element, the link entity cfProj_OrgUnit. The XML record of cfProj B must be available through both sets **openaire_cris** and **openaire_cris_projects**.

In case the two entity instances (cfOrgUnit A and cfProj B) are retrieved via the different sets **openaire_cris_orgunits** and **openaire_cris_projects**, the OAI-PMH service provider – in this case the OpenAIRE infrastructure – should combine and check the information in the two different sets of XML records to validate the source data in terms of referential integrity.


Transmission of CERIF XML as OAI-PMH payload
""""""""""""""""""""""""""""""""""""""""""""

OAI-PMH is a protocol for exposing information from data providers to clients (service providers). Data provided through OAI-PMH must be encoded in XML and is organised into a sequence of records. The protocol uses the resumption token mechanism to enable control over the flow of data from the data provider towards the service provider, for example, it allows the split of a large chunk of records into fragments of manageable size (e.g. 100 records). This helps avoid overload of both the data and service provider.

Data in CERIF CRIS systems follows a normalised graph structure. Therefore, the transmission of CERIF XML as OAI-PMH payload requires a mechanism of fitting the graph structure into a sequence of records. The CERIF XML structure should be decomposed into a sequence of XML records. Each OAI-PMH XML record should represent a single instance of a CERIF Research Entity, embedding multi-lingual entities, federated identifiers and link entities, but with no nested records for other CERIF Research Entity instances. 

**Date stamps in CERIF XML records**

In OAI-PMH, selective harvesting based on last-update date stamps on records is possible, so that only records that have been modified since the last harvesting are retrieved. Due to considerations regarding not consistent and reliable mechanisms for setting date stamp values in certain source systems, OpenAIRE in the general case tends to avoid employing selective harvesting based on last update dates. If reliable mechanisms for setting date stamps are present in a source CRIS system, OpenAIRE may employ selective harvesting, for example in the case of very large data sources.  

The following rules apply regarding setting values of date stamps for CERIF XML records exposed by CRIS systems to OpenAIRE via OAI-PMH: 

Datestamps should be set by CRIS systems in records, based on the following last update principle: the date stamp should reflect the last date/time where any information contained within the record payload (e.g. entity fields, multilingual fields, federated identifiers, linked entities). Any such modification should result in a modification of the date stamp; under no circumstances can the date stamp be earlier than this date. 
For example, we assume a CERIF XML record of type cfProj, containing:

1. Entity fields (e.g. cfProj.cfAcro)
2. Multilingual fields (e.g. cfProj.cfTitle)
3. Federated identifiers (e.g. grant agreement number in the case of EU FP7 projects).
4. Linked entities (e.g. link entities cfProj_OrgUnit denoting participation of organisations to the project)

Let us consider the database underlying the CRIS system from which the CERIF XML is exported. Example update cases of the cfProj instance information in the database are provided in the following list, along with the corresponding date stamp modifications of the cfProj CERIF XML record:

a. cfProj.cfAcro is modified. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
b. An existing cfProj.cfTitle instance is modified, e.g. update of cfProj.cfTitle. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
c. A new cfProj.cfTitle is added to this cfProj instance (e.g. the project title in another language). The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the addition.
d. An existing federated identifier instance referring to this cfProj instance is modified, e.g. update of the cfProj.cfFedId.startDate. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
e. An existing federated identifier instance classification referring to this cfProj instance is modified, e.g. update of the cfFedId_Class.cfEndDate. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
f. An existing cfFedId_Srv linked entity instance, concerning a federated identifier referring to this cfProj instance is modified, e.g. update of the cfFedId_Srv.cfStartDate. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
g. An existing cfSrv instance is modified (e.g. cfSrv.cfURI). This particular cfSrv instance concerns a service that has issued a federated identifier referring to this cfProj instance. In this case, the date stamp of the respective cfProj CERIF XML record must NOT be updated to the date/time of the modification.
h. A new federated identifier is added for this cfProj instance. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the addition.
i. A new cfProj_OrgUnit instance is added to the database, linking the cfProj instance to an organisation that participates in the project. The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the addition.
j. An existing cfProj_OrgUnit link entity instance is modified (e.g.  cfProj_OrgUnit.cfStartDate). The date stamp of the respective cfProj CERIF XML record must be updated to the date/time of the modification.
k. An existing cfOrgUnit instance is modified (e.g. cfOrgUnit.cfAcro). This particular cfOrgUnit instance concerns an organization that is a partner in the project and thus is already connected with the cfProj through a cfProj_OrgUnit linked entity. In this case, the date stamp of the respective cfProj CERIF XML record must NOT be updated to the date/time of the modification.

**Deleted records**

OpenAIRE does **not** require CRIS systems to provide information about deleted records via OAI-PMH. Therefore, it is acceptable for a CRIS system exposing metadata records to the OpenAIRE infrastructure to provide any of the three levels of support of deleted records, as defined in the OAI-PMH 2.0 specification: “**no**”, “**persistent**” or “**transient**”. As mandated in the OAI-PMH 2.0 specification, CRIS systems must declare the level of support of deleted records in the deletedRecord element of the Identify response.
