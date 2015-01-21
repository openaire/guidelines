==RelatedIdentifier==
{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (if different from DataCite)
|-
| 12 || RelatedIdentifier || MA || ''Mandatory when applicable'' property in OpenAIRE instead of recommended in DataCite.

Please refer to the section “Related publications and datasets information” below for specific details on how to link datasets and publications.

|-
| 12.1 || relatedIdentifierType || MA || -
|-
| 12.2 || relationType || MA || ''Controlled List''
Allowed values (recommended ones, please refer to DataCite Metadata Schema v2.2 for a complete list)

<u>IsCitedBy</u> (indicates that B includes A in a citation)
Cites (indicates that A includes B in a citation)
<u>IsSupplementTo</u> (indicates  that A is a supplement to B)
<u>isSupplementedBy</u> (indicates that B is a supplement to A)
<u>IsPartOf</u> (indicates A is a portion of B; may be used for elements of a series)
HasPart</u> (indicates A includes the part B)
<u>IsNewVersionOf</u> (indicates A is a new edition of B, where the new edition has been modified or updated)
<u>IsPreviousVersionOf</u> (indicates A is a previous edition of B)

'''Note''': ''Cites'' and ''IsCitedBy'' is specifically for when a publication/dataset directly cites another publication/dataset in its references, whereas ''References'' and ''IsReferencedBy'' is for when a dataset/publication is used as a source of information without a direct citation.

OpenAIRE encourages including minimum one of above listed relation types, but allows usage of all DataCite’s relation types.

|-
| 12.3 || relatedMetadataSchema || O || -
|-
| 12.4 || schemeURI || O || -
|-
| 12.5 || schemeType || O || -
|-
|}

==Definition==

===RelatedIdentifier===
Identifiers of related resources.

'''Occurrences''': 0-n

===relatedIdentifierType (attribute) ===
The type of the ''RelatedIdentifier''.

'''Occurrences''': Required

===relationType (attribute) ===

Description of the relationship of the resource being registered (A) and the related resource (B).

'''Occurrences''': Required

===relatedMetadataScheme (attribute) ===

The name of the scheme.

'''Occurrences''': 0-1

===schemeURI (attribute) ===

The URI of the relatedMetadataScheme.

'''Occurrences''': 0-1

===schemeType (attribute) ===

The type of the relatedMetadataScheme, linked with the schemeURI.

'''Occurrences''': 0-1

==Allowed values (DataCite)==

===RelatedIdentifier===

The format is open.

Use this property to indicate subsets of properties, as appropriate.

===relatedIdentifierType===

'''Controlled List'''
Allowed values:
* ARK
* DOI
* EAN13
* EISSN
* Handle
* ISBN
* ISSN
* ISTC
* LISSN
* LSID
* PURL
* UPC
* URL
* URN

===relationType ===

''Controlled List''
Allowed values:
* <u>IsCitedBy</u> (indicates that B includes A in a citation)
* <u>Cites</u> (indicates that A includes B in a citation)
* <u>IsSupplementTo</u> (indicates that A is a supplement to B)
* <u>IsSupplementedBy</u> (indicates that B is a supplement to A)
* <u>IsContinuedBy</u> (indicates A is continued by the work B)
* <u>Continues</u>(indicates A is a continuation of the work B)
* <u>IsNewVersionOf</u> (indicates A is a new edition of B, where the new edition has been modified or updated)
* <u>IsPreviousVersionOf</u> (indicates A is a previous edition of B)
* <u>IsPartOf</u> (indicates A is a portion of B;may be used for elements of a series)
* <u>HasPart</u> (indicates A includes the part B)
* <u>IsReferencedBy</u> (indicates A is used as a source of information by B)
* <u>References</u>(indicates B is used as a source of information for A)
* <u>IsDocumentedBy</u> (indicates B is documentation about/explaining A)
* <u>Documents</u> (indicates A is documentation about/explaining B)
* <u>isCompiledBy</u> (indicates B is used to compile or create A)
* <u>Compiles</u>(indicates B is the result of a compile or creation event using A)
* <u>IsVariantFormOf</u> (indicates A is a variant or different form of B, e.g. calculated or calibrated form or different packaging)
* <u>IsOriginalFormOf</u> (indicates A is the original form of B)

===relatedMetadataScheme===

Use only with this relation pair: (HasMetadata/IsMetadataFor)

===schemeURI===

Use only with this relation pair: (HasMetadata/IsMetadataFor)

===schemeType===

Use only with this relation pair: (HasMetadata/IsMetadataFor)

Examples: XSD, DDT, Turtle

==OpenAIRE==

''Controlled List''
Allowed values (recommended ones, please refer to DataCite Metadata Schema v2.2 for a complete list - see above)

* <u>IsCitedBy</u> (indicates that B includes A in a citation)
* <u>Cites</u> (indicates that A includes B in a citation)
* <u>IsSupplementTo</u> (indicates that A is a supplement to B)
* <u>IsSupplementedBy</u> (indicates that B is a supplement to A)
* <u>IsPartOf</u> (indicates A is a portion of B; may be used for elements of a series)
* <u>HasPart</u> (indicates A includes the part B)
* <u>IsNewVersionOf</u> (indicates A is a new edition of B, where the new edition has been modified or updated)
* <u>IsPreviousVersionOf</u> (indicates A is a previous edition of B)

'''Note''': ''Cites'' and ''IsCitedBy'' is specifically for when a publication/dataset directly cites another publication/dataset in its references, whereas ''References'' and ''IsReferencedBy'' is for when a dataset/publication is used as a source of information without a direct citation.

OpenAIRE encourages including minimum one of above listed relation types, but allows usage of all DataCite’s relation types.

=== Related publications and datasets information ===
OpenAIRE '''harvests all datasets''' from a data repository, but '''exposes only certain datasets''' in the OpenAIRE portal. See the section “OpenAIRE OAI Set” below for specific details of which datasets are exposed.

For example, datasets related to publication will be exposed in the OpenAIRE portal. The link between the dataset and publication may be explicit defined, as described in this section below, or automatically inferred by the OpenAIRE infrastructure. If the link is explicit defined, the dataset will be exposed in the OpenAIRE portal '''within 1-2 days after harvesting''' (a repository is harvested once a week on average). If the link is automatically inferred by the OpenAIRE infrastructure it may take '''up to a month after harvesting''' before the dataset is exposed in the OpenAIRE portal. It is thus mandatory when applicable to provide links to related publications and datasets when these links are available in the repository, and thereby ensure faster exposure of the dataset in the OpenAIRE portal.

DataCite Metadata Schema allows linking publications and datasets by use of persistent identifiers to uniquely identify the resource being described (A) typically a dataset but not limited to that, and the related resource (B) in the case of OpenAIRE typically a publication or a dataset.

==XML example==
<code>
 <relatedIdentifiers>
  <relatedIdentifier relatedIdentifierType="DOI" relationType="IsCitedBy">10.1234/bar</relatedIdentifier>
  <relatedIdentifier relatedIdentifierType="URN" relationType="Cites">http://testing.ts/testpub</relatedIdentifier>
 </relatedIdentifiers>
</code>

==Comments==
<comments />
