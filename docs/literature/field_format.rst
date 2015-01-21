== Field Name ==
format
== DC Field ==
<code>dc:format</code>

== Usage ==
''Recommended''

== DCMI Definition ==
The physical or digital manifestation of the resource. Typically, Format may include the media-type or dimensions of the resource. Format may be used to determine the software, hardware or other equipment needed to display or operate the resource. Examples of dimensions include size and duration. Recommended best practice is to select a value from a controlled vocabulary (for example, the list of Internet Media Types [MIME] defining computer media formats).
== Usage Instruction ==
Based on best practice, the IANA registered list of Internet Media Types (MIME types) is used to select a term from. For the full list see http://www.iana.org/assignments/media-types

If one specific resource (an instance of scientific output) has more than one physical formats (e.g. postscript and pdf) stored as different object files, all formats are mentioned in the DC element format, for example:

* <code><dc:format>application/pdf</dc:format></code>
* <code><dc:format>application/postscript</dc:format></code>
* <code><dc:format>application/vnd.oasis.opendocument.text</dc:format></code>
== Do Not Confuse With ==
* [[Literature_Guidelines:_Metadata_Field_Publication_Type|dc:type]]
* [[Literature_Guidelines:_Metadata_Field_Resource_Identifier|dc:identifier]]
DC element ‘format’ describes the media type of this resource. DC element ‘type’ describes the kind of academic output the resource is a representation of. dc:identifier is used to represent manifestations of digital resources.
== Since ==
DRIVER Guidelines v2

== Examples ==
<pre>
<dc:format>video/quicktime</dc:format>
<dc:format>application/pdf</dc:format>
<dc:format>application/xml</dc:format>
<dc:format>application/xhtml+xml</dc:format>
<dc:format>application/html</dc:format>
<dc:format>application/vnd.oasis.opendocument.text</dc:format>
</pre>

==Comments==
<comments/>
