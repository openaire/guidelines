==Title==
{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (in '''bold''' if different from DataCite)
|-
| 3 || Title|| M || -
|-
| 3.1 || titleType|| O || -
|-
|}

==Definition==
===Title===
'''Title''' is a name or title by which the resource is known

Title can be repeated and titleType is an optional specification of the title property.

'''Occurrences''': 1-n

===titleType (attribute)===
The type of Title.

'''Occurrences''': Optional

==Allowed values (DataCite)==
===Title===
The format is open.

===titleType===
''Controlled List''
Allowed values:
* Alternative Title
* Subtitle
* TranslatedTitle

==OpenAIRE==
There are no OpenAIRE requirements for this property.

==XML example==
<code>
 <titles>
  <title>
   National Institute for Environmental Studies and Center for Climate System Research Japan
  </title>
  <title titleType="Subtitle">A survey</title>
 </titles>
</code>

==Comments==
<comments/>
