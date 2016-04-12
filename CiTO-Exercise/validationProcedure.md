# CiTO Metadata: Validation of Notation 3 metadata files.
(Creation date: 2016-04-06)

## The first step is creating the two CiTO files:
    presentationMetadata.n3 and
    citationMetadata.n3 .

Start by making a copy of the metadata template files and editing it
to reflect your presentation and citations. The key elements to change
to match your work include (but are not limited to):

(1) the template elements that are in all caps, such as
YOURPROJECTTITLEHERE, etc.;

(2) the keywords that are in the "dc:subject" predicate in the
presentationMetadata file; and

(3) the CiTO predicate that is used for each of your citations in the
citationMetadata file. The predicates to use are found in this document:
http://vocab.ox.ac.uk/cito .

Privacy Note: any place a URI is required, for example the
"foaf:workplaceHomePage" object, you can use http://example.com as the
scheme part. You can use YOURINITIALS@example.com wherever
YOUREMAILHERE appears.

## Validating the CiTO files:

The procedure for determing if the CiTO Notation3 metadata files are valid has
two steps. This procedure has been used to validate the CiTO
presentationMetadata.n3 and citationMetadata.n3 template files.

Suggested method: open two tabs in a web browser.

In the first tab fetch the RDF Translator:
   http://rdf-translator.appspot.com
In the second tab fetch the W3C Validation Service:
   https://www.w3.org/RDF/Validator/


(1) Convert the N3 CiTO files to RDF/XML using the "Input Field" of the
RDF Translator (tab 1). Use the "Copy to Clipboard..." button to copy the
resulting RDF/XML output to the clipboard.

(If you wish (not necessary) you can save the RDF/XML output in another file.)


(2) Validate the RDF/XML document with the W3C Validation Service (tab 2) by
pasting the RDF/XML output into the "Check by Direct Input"
field. Select "Triples Only" in the "Display Result Options" drop-down
menu. Then select the "Parse RDF" button. If your RDF/XML is valid the
validation service returns with the triples in a table and above the
table the message "Your RDF document validated successfully."

(3) If your document does not validate successfully then you need to
use the error messages to find the problem. It might be only a syntax
error in the n3 file such as a missing comma or semicolon in a triple,
a missing period at the end of a triple, or an error in a URI.
