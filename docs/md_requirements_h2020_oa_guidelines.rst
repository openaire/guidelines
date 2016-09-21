.. _h2020:

How the Horizon 2020 Open Access requirements are met
=====================================================

The European Commission has published `Guidelines on Open Access to Scientific Publications and Research Data <http://ec.europa.eu/research/participants/data/ref/h2020/grants_manual/hi/oa_pilot/h2020-hi-oa-pilot-guide_en.pdf>`_ (version 1.0, 11-Dec-2013).

In addition to basic bibliographic information about deposited publications extra information is expected in the following fields:

Property 'EU funding acknowledgement'
-------------------------------------

DC Field
~~~~~~~~
``dc:contributor``


Usage Instruction
~~~~~~~~~~~~~~~~~

Values for this field must include one of the following applicable terms:

* ``["European Union (EU)" and "Horizon 2020"]``
* ``["Euratom" and "Euratom research and training programme 2014-­2018"]``

Property 'Peer Reviewed'
------------------------

DC Field
~~~~~~~~
``dc:type``

Usage Instruction
~~~~~~~~~~~~~~~~~

``info:eu-repo/semantics/publishedVersion``


Property 'Embargo Period'
-------------------------

If the research outcome is published under an embargo please specify the embargo end date and the embargoed access mode.

DC Field
~~~~~~~~
``dc:date``

Usage Instruction
~~~~~~~~~~~~~~~~~

``info:eu-repo/date/embargoEnd/<YYYY-MM-DD>``

DC Field
~~~~~~~~
``dc:rights``

Usage Instruction
~~~~~~~~~~~~~~~~~

``info:eu-repo/semantics/embargoedAccess``

Property 'Project Information'
------------------------------

DC Field
~~~~~~~~
``dc:relation``

Usage Instruction
~~~~~~~~~~~~~~~~~

``info:eu-repo/grantAgreement/Funder/FundingProgram/ProjectID/[Jurisdiction]/[ProjectName]/[ProjectAcronym]/``

Example
~~~~~~~

Project information for the OpenAIRE2020 project would be encoded as:

``<dc:relation>info:eu-repo/grantAgreement/EC/H2020/643410/EU/OpenAIRE2020/OpenAIRE2020/``


Property 'Publication Date'
---------------------------

DC Field
~~~~~~~~
``dc:date``

Usage Instruction
~~~~~~~~~~~~~~~~~

Property 'Persistent Identifier for the Research Outcome'
---------------------------------------------------------

DC Field
~~~~~~~~
``dc:identifier``

``dc:relation``


Usage Instruction
~~~~~~~~~~~~~~~~~



Property 'License'
------------------

DC Field
~~~~~~~~
``dc:rights``

Usage Instruction
~~~~~~~~~~~~~~~~~

It is recommended to provide a URL which provides the location where the license can be read, e.g.:

``http://opendatacommons.org/licenses/by/1.0``

Property 'Persistent Identifiers for Authors / Contributors'
------------------------------------------------------------

DC Field
~~~~~~~~
``dc:creator``

``dc:contributor``

Usage Instruction
~~~~~~~~~~~~~~~~~

``Lastname, Firstname; id_orcid 0000-0000-0000-0000``

Property 'Reference to related research outcome'
------------------------------------------------

DC Field
~~~~~~~~
``dc:relation``

Usage Instruction
~~~~~~~~~~~~~~~~~

``info:eu-repo/semantics/dataset/<scheme>/<id>``

