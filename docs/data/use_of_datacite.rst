== DataCite ==
OpenAIRE has adopted the DataCite Metadata Schema as the basis for harvesting and importing metadata about datasets from data archives.

The core mission of DataCite is to build and maintain a sustainable framework that makes it possible to cite data through the use of persistent identifiers, DOIs.

OpenAIRE shares the goal of the DataCite Metadata Schema - to provide a domain agnostic metadata schema and provide interoperability through a small number of properties - making interoperability possible in the simplest manner possible and as a result keep the technical barriers for implementation as low as possible.

We would like to thank DataCite for their kind support and help making these OpenAIRE Guidelines for Data Archive Managers possible.

== What’s different ==
In this document you will find the needed properties to make your data archive compatible with the OpenAIRE infrastructure. OpenAIRE has adopted the DataCite Metadata Schema version 3.0 with some minor adjustments.

* OpenAIRE accepts other persistent identifier schemes and not only a DOI in 1.1 [[Data_Guidelines:_Metadata_Property_Identifier|identifierType]].
* OpenAIRE recommends exporting links to related publications and datasets (i.e. 12. [[Data_Guidelines:_Metadata_Property_RelatedIdentifier|RelatedIdentifier]] property and attributes are mandatory when applicable).
* OpenAIRE recommends using the 7. [[Data_Guidelines:_Metadata_Property_Contributor|Contributor]] property to relate a dataset to funding information.
* DataCite optional properties 8. [[Data_Guidelines:_Metadata_Property_Date|Date]] and 17. [[Data_Guidelines:_Metadata_Property_Description|Description]] are mandatory in OpenAIRE.
* OpenAIRE enforces an encoding scheme on DataCite property 16. [[Data_Guidelines:_Metadata_Property_Rights|Rights]].
 

== OpenAIRE application of DataCite Metadata Schema ==
OpenAIRE builds on the DataCite Metadata Schema v3.0 by making some of the otherwise optional DataCite properties mandatory, as well as enforcing specific encoding schemes on the values of some DataCite properties. The table below details the differences from the DataCite Metadata Schema.

Within OpenAIRE the use of properties are either:
* mandatory (M) = the property must always be present in the metadata record. An empty property is not allowed.
* mandatory when applicable (MA) = when the property can be obtained it must be present in the metadata record
* recommended (R) = the use of the property is recommended
* optional (O) = the property may be used to provide complementary information about the resource

The recommended status is made primarily to encourage users to input certain properties when creating a metadata record to enhance services.

==Comments==
<comments/>
