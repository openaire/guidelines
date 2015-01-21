==Rights==
{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (if different from DataCite)
|-
| 16 || Rights || MA || ''Mandatory when applicable'' property in OpenAIRE instead of optional in DataCite.

Free text (see 16.1 rightsURI).

OpenAIRE uses this property to explicit declare the access right of the resource via 16.1 rightsURI. This does not exclude also using 16. Rights property for additional rights statements as defined by DataCite Metadata Schema v3.0. In particular OpenAIRE also recommends including license information if available.

Please refer to the section “Access right and license information” below for a full example of how to declare access right and license information.

|-
| 16.1 || rightsURI || MA || ''Mandatory when applicable'' property in OpenAIRE instead of optional in DataCite.

Use terms from the info:eu-repo-Access-Terms vocabulary<ref>See http://purl.org/eu-repo/semantics/#info-eu-repo-AccessRights </ref>. The values are
* <code>info:eu-repo/semantics/closedAccess</code>
* <code>info:eu-repo/semantics/embargoedAccess</code>
* <code>info:eu-repo/semantics/restrictedAccess</code>
* <code>info:eu-repo/semantics/openAccess</code>

This property may also be used to explicitly declare the license for the resource.

Please refer to the section “Access right and license information” below for a full example of how to declare access right and license information.
|-
|}

==Definition==

===Rights===
Any rights information for this resource.

'''Occurrences''': 0-n

===rightsURI (attribute)===
The URI of the license

'''Occurrences''': 0-1

==Allowed values (DataCite)==

===Rights===
The format is open.

Provide a rights management statement for the resource or reference a service providing such information. Include embargo information if applicable.

Use the complete title of a license and include version information if applicable.

Example:
Creative Commons Attribution 3.0 Germany License

===rightsURI (attribute)===

Example:
http://creativecommons.org/licenses/by/3.0/de/deed.en

==OpenAIRE==

OpenAIRE uses the access rights to enable a better user experience by declaring the access rights clear and explicit in the portal, using terms from the info:eu-repo-Access-Terms vocabulary<ref>See http://purl.org/eu-repo/semantics/#info-eu-repo-AccessRights</ref>.

==XML example==

<code>
  <rightsList>
    <rights rightsURI=”info:eu-repo/semantics/openAccess” />
  </rightsList>
</code>

OpenAIRE further recommends including license information if available:

<code>
  <rightsList>
    <rights rightsURI=”info:eu-repo/semantics/openAccess” />
    <rights rightsURI=”http://creativecommons.org/licenses/by/4.0/”>
      Creative Commons Attribution 4.0 International
    </rights>
  </rightsList>
</code>

==Comments==
<comments/>
