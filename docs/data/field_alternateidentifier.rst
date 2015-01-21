==AlternateIdentifier==
{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (if different from DataCite)
|-
| 11 || AlternateIdentifier || O || -
|-
| 11.1 || alternateIdentifierType || O || -
|-
|}

==Definition==
===AlternateIdentifier===
An identifier or identifiers other than the primary Identifier applied to the resource being registered. This may be any alphanumeric string which is unique within its domain of issue.

'''Occurrences''': 0-n

===alternateIdentifierType (attribute) ===
The type of the ''AlternateIdentifier''.

'''Occurrences''': Required

==Allowed values (DataCite)==

===AlternateIdentifier===
The format is open.

===alternateIdentifierType===
The format is open.

==OpenAIRE==
There are no OpenAIRE requirements for this property.

==XML example==
<code>
 <alternateIdentifiers>
  <alternateIdentifier alternateIdentifierType="ISBN">937-0-1234-56789-X</alternateIdentifier>
 </alternateIdentifiers>
</code>

==Comments==
<comments />
