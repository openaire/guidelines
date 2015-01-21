==Creator==
{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (if different from DataCite)
|-
| 2 || Creator || M || -
|-
| 2.1 || creatorName || M || -
|-
| 2.2 || nameIdentifier || R || -
|-
| 2.2.1 || nameIdentifierScheme || R || OpenAIRE recommends including a nameIdentifier such as an ORCID or a ISNI if available.
|-
| 2.2.2 || schemeURI || O || -
|}

==Definition==

===Creator===
The main researchers involved in producing the data, or the authors of the publication, in priority order.

'''Occurrences''': 1-n

===creatorName (child) ===
The name of the creator

'''Occurrences''': 1

===nameIdentifier (child) ===

Uniquely identifies an individual or legal entity, according to various schemes.

'''Occurrences''': 0-1

===nameIdentifierScheme (attribute) ===

The name and/or the URL of the name identifier scheme.

'''Occurrences''': Required

=== schemeURI (attribute) ===

The URI of the name identifier scheme.

'''Occurrences''': Optional

==Allowed values (DataCite)==
===Creator===
May be a corporate/institutional or personal name. The personal name format should be:
family, given. Non‐roman names should be transliterated according to the ALA‐LC schemes found at http://www.loc.gov/catdir/cpso/roman.html

===creatorName ===

Examples: Toru, Nozawa; Utor, Awazon

===nameIdentifier ===

The format is dependent upon scheme.

===nameIdentifierScheme ===

Examples are Open Researcher and Contributer ID (ORCID), International Standard Name Identifier (ISNI).

==OpenAIRE==
There are no OpenAIRE requirements for this property.

==XML example==
<code>
 <creators>
  <creator>
   <creatorName>Miller, John</creatorName>
  </creator>
  <creator>
   <creatorName>Smith, Jane</creatorName>
   <nameIdentifier nameIdentifierScheme="ISNI" schemeURI="http://www.isni.org">1422 4586 3573 0476</nameIdentifier>
  </creator>
 </creators>
</code>

==Comments==
<comments/>
