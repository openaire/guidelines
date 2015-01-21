==Identifier==
{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (in '''bold''' if different from DataCite)
|-
| 1 || Identifier || M || DOI (Digital Identifier) is preferred. The format should be "10.1234/foo".
|-
| 1.1 || IdentifierType || M || Unlike DataCite, OpenAIRE allows for DOIs and other types of identifiers.
|-
|}

==Definition==

===Identifier===
The ''Identifier'' is a unique string that identifies a resource.

'''Occurrences''': 1

===identifierType (attribute)===
The type of the Identifier.

'''Occurrences''': Required

==Allowed values (DataCite)==
''Controlled List''
Allowed values:
* DOI

NB! OpenAIRE allows for other types of identifiers, see below.

==OpenAIRE==
Unlike DataCite, OpenAIRE allows for DOIs and other types of identifiers.

''Controlled List''
Allowed values:
* ARK
* DOI
* Handle
* PURL
* URN
* URL

==XML example==
<code>
 <identifier identifierType="DOI">10.1594/WDCC/CCSRNIES_SRES_B2</identifier>
</code>

==Comments==
<comments/>
