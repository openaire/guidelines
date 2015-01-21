==ResourceType==
{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (if different from DataCite)
|-
| 10 || ResourceType|| R || OpenAIRE strongly recommends use of ResourceType and the sub-property resourceTypeGeneral.
|-
| 10.1 || resourceTypeGeneral|| R || -
|-
|}

==Definition==
===ResourceType===
A description of the resource.

'''Occurrences''': 0-1

===resourceTypeGeneral (attribute) ===
The general type of a resource.

'''Occurrences''': Required

==Allowed values (DataCite)==
===ResourceType===
The format is open, but the preferred format is a single term of some detail so that a pair can be formed with the attribute.

Example: Image/Animation, where 'Image' is ''resourceTypeGeneral'' value and 'Animation'
is ''ResourceType'' value.

===resourceTypeGeneral===
''Controlled List''
Allowed values:
* Collection
* Dataset
* Event
* Film
* Image
* InteractiveResource
* Model
* PhysicalObject
* Service
* Software
* Sound
* Text

==OpenAIRE==
There are no OpenAIRE requirements for this property.

==XML example==
<code>
 <resourceType resourceTypeGeneral="Image">Animation</resourceType>
</code>

<comments/>
