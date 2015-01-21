==OpenAIRE-specific Syntax for OAI-DC==
OpenAIRE relies on a specific syntax used in the values of standard Dublin Core metadata fields to identify projects, funders, referenced publications, and datasets. This syntax takes the form of URIs and is defined as the info:eu-repo namespace.

This section explains which DC fields to use together with this syntax to correctly mark up the information relevant for OpenAIRE.

Within OpenAIRE the use of the fields is either:

* '''Mandatory (M)''' = the field must always be present in the metadata record. An empty element is not allowed.
* '''Mandatory when applicable (MA)''' = when the value of the field can be obtained it must be present in the metadata record.
* '''Recommended (R)''' = the use of the field is recommended.
* '''Optional (O)''' = it is not important whether the element is used or not.

=== A complete example record ===

<code>

    <record>
        <header>
            <identifier>oai:repository.example.com:2003292</identifier>
            <datestamp>2012-11-30T13:40:28Z</datestamp>
            <setSpec>openaire</setSpec>
        </header>
        <metadata>
            <oai_dc:dc xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:oai_dc="http://www.    openarchives.org/OAI/2.0/oai_dc/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi :schemaLocation="http://www.openarchives.org/OAI/2.0/oai_dc/ http://www.openarchives.    org/OAI/2.0/oai_dc.xsd">
                <dc:title>Studies of Unicorn Behaviour</dc:title>
                <dc:identifier>http://repository.example.org/2003292</dc:identifier>
                <dc:creator>Jane, Doe</dc:creator>
                <dc:creator>John, Doe</dc:creator>
                <dc:description>
                    Lorem ipsum dolor...
                </dc:description>
                <dc:subject>info:eu-repo/classification/ddc/590</dc:subject>
                <dc:subject>Unicorns</dc:subject>
                <dc:relation>info:eu-repo/grantAgreement/EC/FP7/1234556789/EU//UNICORN</dc:relation>
                <dc:relation>info:eu-repo/semantics/altIdentifier/eissn/1234-5678</dc:relation>
                <dc:relation>info:eu-repo/semantics/altIdentifier/pmid/123456789</dc:relation>
                <dc:relation>info:eu-repo/semantics/altIdentifier/doi/10.1000/182</dc:relation>
                <dc:relation>info:eu-repo/semantics/reference/doi/10.1234/789.1</dc:relation>
                <dc:relation>info:eu-repo/semantics/dataset/doi/10.1234/789.1</dc:relation>
                <dc:rights>info:eu-repo/semantics/openAccess</dc:rights>
                <dc:rights>http://creativecommons.org/licenses/by-sa/2.0/uk/</dc:rights>
                <dc:source>Journal Of Unicorn Research</dc:source>
                <dc:publisher>Unicorn Press</dc:publisher>
                <dc:date>2013</dc:date>
                <dc:type>info:eu-repo/semantics/article</dc:type>
            </oai_dc:dc>
        </metadata>
    </record>

</code>

==Comments==
<comments/>
