==Date==
{| class="wikitable"
|-
! ID !! DataCite-property !! Status !! Encoding schemes (if different from DataCite)
|-
| 8 || Date || M || ''Mandatory'' property in OpenAIRE instead of ''recommended'' in DataCite. For encoding scheme, please refer to DataCite Metadata Schema v3.0 for details.
|-
| 8.1 || dateType || M || Use “Issued” for the date the resource is published or distributed. To indicate the end of an embargo period, use “Available”. To indicate the start of an embargo period, use “Accepted”.

DataCite v3.0 further recommends use of “Created” and “Submitted”.

Further dateTypes may be specified. Please refer to DataCite Metadata Schema v3.0 for details.

|-
|}

==Definition==

===Date===
Different dates relevant to the work.

Please refer to the OpenAIRE specification - the property is not ''optional'' as in the DataCite schema but ''mandatory'' in OpenAIRE.

'''Occurrences''': 0-n (DataCite), 1-n (OpenAIRE)

===dateType (attribute) ===
The type of date.

'''Occurrences''': Required

==Allowed values (DataCite)==
===Date===
YYYY or YYYY‐MM‐DD

or any other format described in [http://www.w3.org/TR/NOTE%E2%80%90datetime W3CDTF]

May be repeated to indicate a date range.

===dateType===
''Controlled List''
Allowed values:
* Accepted (The date that the publisher accepted the resource into their system.)
* Available (The date the resource is made publicly available. May be a range.)
* Copyrighted (The specific, documented date at which the resource receives a copyrighted status, if applicable.)
* Created (The date the resource itself was put together; this could be a date range or a single date for a final component, e.g.,the finalised file with all of the data.)
* EndDate (Use if any other date type covers a range)
* Issued (The date that the resource is published or distributed e.g.to a data center.)
* StartDate (Use if any other date type covers a range)
* Submitted (The date the creator submits the resource to the publisher. This could be different from Accepted if the publisher then applies a selection process.)
* Updated (The date of the last update to the resource, when the resource is being added to. May be a range.)
* Valid (The date or date range during which the dataset or resources are accurate. May be a range.)


To indicate a date period, provide two dates,
specifying the StartDate and the EndDate. To
indicate the end of an embargo period, use
Available. To indicate the start of an
embargo period, use Submitted or Accepted,
as appropriate.

==OpenAIRE==
Date is a ''mandatory'' property in the OpenAIRE application profile.

Use “Issued” for the date the resource is published or distributed.

To indicate the end of an embargo period, use “Available”. To indicate the start of an embargo period, use “Accepted”.

Further dateTypes may be specified. Please refer to "Allowed values (DataCite)" above.

===Embargo date information===
For OpenAIRE two main types of dates are relevant. When the data were made available, published or uploaded to a formal database, this is the date the data were ''Issued''.

Sometimes data may be embargoed for a period; this information should be managed by the data provider and expressed by exporting an ''Available'' date to indicate the end of an embargo period and an ''Accepted'' date to indicate the start of an embargo period.

==XML example==

'''Example:'''
<code>
 <dates>
  <date dateType="Issued">2005-04-05</date>
 </dates>
</code>

'''An embargo example:'''
<code>
 <dates>
  <date dateType="Accepted">2011-12-01</date>
  <date dateType="Available">2012-12-01</date>
 </dates>
</code>

==Comments==
<comments />
