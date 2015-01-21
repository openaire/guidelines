== Field Name ==
publication type
== DC Field ==
<code>dc:type</code>

== Usage ==
Publication type is used for the following purposes:
# ''Mandatory'': Publication type (controlled): to indicate the type of publication based on the info:eu-repo-publication-type-terms vocabulary
# ''Optional'': Publication type (free): to indicate the type of publication based on a local repository vocabulary

== DCMI Definition ==
The type of scientific output the resource is a manifestation of. In the DC element type the kind of dissemination, or the intellectual and/or content type of the resource is described. It is used to explain to the user what kind of resource he is looking at. Is it a book or an article. Was it written for internal or external use, etc.

== Usage Instruction ==
'''Publication types (controlled):'''

The first occurrence of the DC Element ‘type’ is mandatory and should be used for the type indication of the scientific output based on the info:eu-repo publication type vocabulary:

* <code>info:eu-repo/semantics/article</code>
* <code>info:eu-repo/semantics/bachelorThesis</code>
* <code>info:eu-repo/semantics/masterThesis</code>
* <code>info:eu-repo/semantics/doctoralThesis</code>
* <code>info:eu-repo/semantics/book</code>
* <code>info:eu-repo/semantics/bookPart</code>
* <code>info:eu-repo/semantics/review</code>
* <code>info:eu-repo/semantics/conferenceObject</code>
* <code>info:eu-repo/semantics/lecture</code>
* <code>info:eu-repo/semantics/workingPaper</code>
* <code>info:eu-repo/semantics/preprint</code>
* <code>info:eu-repo/semantics/report</code>
* <code>info:eu-repo/semantics/annotation</code>
* <code>info:eu-repo/semantics/contributionToPeriodical</code>
* <code>info:eu-repo/semantics/patent</code>
* <code>info:eu-repo/semantics/other</code>

'''Publication types (free text):'''

The second occurrence of the DC Element ‘type’ is optional and should be used for the subtype indication of the scientific output.

== Do Not Confuse With ==
*  [[Literature_Guidelines:_Metadata_Field_Format|dc:format]]
DC element ‘type’ describes the kind of academic output the resource is a representation of. DC element ‘format’ describes the media type of this resource.

== Since ==
DRIVER Guidelines v2

== Examples ==
<pre>
<dc:type>info:eu-repo/semantics/article</dc:type>
</pre>

==Comments==
<comments/>
