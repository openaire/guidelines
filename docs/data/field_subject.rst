==Subject==
{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (if different from DataCite)
|-
| 6 || Subject|| R || -
|-
| 6.1 || subjectScheme|| O || -
|-
| 6.2 || schemeURI|| O || -
|-
|}

==Definition==

===Subject===
Subject, keyword, classification code, or key phrase describing the resource.

'''Occurrences''': 0-n

===subjectScheme (attribute)===
The subjectScheme used can be announced by its name or by a URL of the Subject scheme.

'''Occurrences''': Optional

===schemeURI (attribute)===
The URI of the subject identifier scheme.

'''Occurrences''': Optional

==Allowed values (DataCite)==

===Subject===
The format is open.

===subjectScheme===
The format is open.

==OpenAIRE==
There are no OpenAIRE requirements for this property.

==XML example==
<code>
 <subjects>
  <subject>Earth sciences and geology</subject>
  <subject subjectScheme="DDC" schemeURI="http://dewey.info/">551 Geology, hydrology, meteorology</subject>
 </subjects>
</code>

==Comments==
<comments/>
