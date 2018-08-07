E-ARK-CSIP
===================================================
*E-ARK Common Specification for Information Packages*

Introduction
------------
This is the GitHub home for all common specification (CS) documentation. This includes:
- the plain text source of the CS;
- all figures and diagrams used in the CS;
- XML schema and schematron used to check CS compliance; and
- archived versions of the CS.

The repository (will) also holds the automated tasks that produce:
- release and release candidate static document, e.g. PDF, versions of the CS for pulication;
- a website version of the common specification: https://dilcisboard.github.io/E-ARK-CSIP/

this includes tasks such as spell checking, formatting, validating the site HTML, testing for broken links, etc.

Getting Started
---------------

### Repository and published GitHub pages
An overview of the repository structure and it's relationship to the website. The published site is generated automatically from GitHub

#### Layout
```
  /
  |-- index.md
  |     Home page for generated GitHub pages site, navigation, etc.
  |
  |-- README.md
  |     This README file
  |
  |-- archive/
  |     Archive directory for old specification versions
    |
    |-- v1_0/
    |     Archive documents for version 1.0 of the common specification
      |
      |-- Common_Specifications_for_IPs_v10.pdf
      |     PDF version of common specification 1.0
      |
      |-- v1_0/
      |     Archive documents for version 1.0 of the common specification
      |  ....
  |-- authors/
  |     http://site.org/authors root for the GitHub pages website
    |
    |-- index.md
    |     Specification authors
    |
  |-- examples/
  |     Package examples, currently empty.
  |     Possibly redundant, why not point to corpus directory?
  |
  |-- history
  |     http://site.org/history/ root for the GitHub pages website
    |
    |-- index.md
    |     Revision history of specification
    |
  |-- implementation/
  |     http://site.org/implementation/ root for the GitHub pages website
    |
    |-- index.md
    |     Implementation section of specification.
    |
  |-- introduction/
  |     http://site.org/introduction/ root for the GitHub pages website
    |
    |-- index.md
    |     Common Specification introduction.
    |
  |-- specification/
  |     http://site.org/specification/ root for the GitHub pages website
    |
    |-- index.md
    |     Page content for http://site.org/specification
    |
  |-- xml/
  |     http://site.org/xml/ root for the GitHub pages website
    |
    |-- DILCISExtensionMETS.xsd
    |-- DILCISVocabularies.rng
    |-- DILCISVocabulariesIP.xml
```
