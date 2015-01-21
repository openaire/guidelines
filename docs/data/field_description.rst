==Description==
{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (if different from DataCite)
|-
| 17 || Description || MA || ''Mandatory when applicable'' property in OpenAIRE instead of optional in DataCite.
|-
| 17.1 || descriptionType || MA || If 17. Description is used, then descriptionType is mandatory.

Use of "Abstract" is ''mandatory when applicable'' in OpenAIRE instead of recommended in DataCite.

Further descriptionType values may be specified. Please refer to DataCite Metadata Schema v3.0 for details.
|-
|}

==Definition==

===Description===

All additional information that does not fit in any of the other categories.

'''Occurrences:''' 0-n

===descriptionType (attribute)===

The type of the description.

'''Occurrences:''' Required

==Allowed values (DataCite)==

===Description===

The format is open.

It is a best practice to supply a description.

===descriptionType===

''Controlled List'' Allowed values:
* Abstract
* SeriesInformation
* TableOfContents
* Other

Use the type SeriesInformation when supplying the description of a resource that is part of a series.

==OpenAIRE==

Mandatory when applicable property in OpenAIRE instead of optional in DataCite.

==XML example==

 <descriptions>
    <description descriptionType="Abstract">This is an abstract</description>
    <description descriptionType="Other">This is e.g. a note.</description>
 </descriptions>

==Comments==
<comments/>
