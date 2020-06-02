% Introduction to XML
% Heinz Wittenbrink
% 2020-06-02

# What is XML?

## XML Basics
- XML: Extensible Markup Language
- Further development of [SGML](https://www.w3.org/MarkUp/SGML/ "Overview of SGML Resources")
- Long understood as an alternative to HTML
- Syntax for XML vocabularies (meta language)
- [W3C Standard](https://www.w3.org/standards/xml/ "XML Technology - W3C")
- Base for a family of further standards and technologies


## Specifications
- Current specification: [Extensible Markup Language (XML) 1.0 (Fifth Edition)](https://www.w3.org/TR/xml/ "Extensible Markup Language (XML) 1.0 (Fifth Edition)") [@paoli2008])
- Many other specifications


## Application areas

- Publishing and management of documents:  Content structuring and flexible presentation
- Web services. Exchange formats for distributed processing on the Internet.


## Document orientation and data orientation

- Document orientation: Mostly semi-structured documents for human addressees
- Data orientation: Highly structured data for clear further processing



## XML: Important properties and terms
- Documents consist of embedded elements. They are "trees" (example for tree view: [XML Online Parser and Viewer](http://countwordsfree.com/xmlviewer "XML Online Parser and Viewer")
- There is one and only one element at the top of the hierarchy, the document or root element.
- Elements must not overlap.
- The XML syntax is the serialization of a hierarchy.
- Attributes must have a value. They are placed in the same order as an element.

## Valid XML
- Valid XML corresponds to the rules of a document type or XML vocabulary
- Practically used XML documents almost always belong to a vocabulary
- Validation is the formal verification of the conformity of a document with the rules
- Document types can be formally defined in document type definitions (DTDs) or through XML or Relax NG schemas
- Example: [Relax NG Schemas for HTML5](http://syntax.whattf.org/ "syntax.whattf.org")

## XML processing
- During XML processing, a parser extracts the relevant information from the document
- This process is standardized, whereby there are different parsers
XML parsers stop processing when a document is not well-formed
- Important form of processing: Transformation with XSLT (Example: [Free Online XSL Transformer (XSLT)](http://www.freeformatter.com/xsl-transformer.html "Free Online XSL Transformer (XSLT) - FreeFormatter.com")

## XML vs. HTML
- XML is case-sensitive, HTML is not
- XML elements must be closed, HTML elements not
- XML attributes must have a name and a value
- HTML specific document type declaration, see https://www.w3.org/QA/2002/04/valid-dtd-list.html
- HTML parsers are more tolerant than XML parsers


## XML Vocabularies on the Web
- [XHTML](https://www.w3.org/TR/xhtml1/) and
Scalable Vector Graphics SVG (https://www.w3.org/Graphics/SVG/)
- MathML (https://www.w3.org/Math/)
- RSS (https://validator.w3.org/feed/docs/rss2.html) and Atom (https://validator.w3.org/feed/docs/atom.html)
- XML Sitemaps
- [Epub](http://idpf.org/epub)


## Example: SVG

[SVG example from Wikipedia](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b1/Beispiel-SVG.svg/800px-Beispiel-SVG.svg.png){width=50%}


## SVG source code:

```XML
<?xml version="1.0" encoding="utf-8" ?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
 "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg width="400" height="400" xmlns="http://www.w3.org/2000/svg" >
 <title>SVG</title>
 <style type="text/css"><! [CDATA
  text {font-size:60px; text-anchor:middle;}
 ]]></style>
 <rect x="0" y="0" height="400" width="400" fill="white" stroke="blue" stroke-width="100" />
 <rect x="160" y="80" width="80" height="240" fill="red" />
 <rect x="80" y="160" width="240" height="80" fill="red" />
 <text x="200" y="220">doctor</text>
</svg>
```

## XML vocabularies for structured documentation

- DocBook (<http://www.docbook.org/>) and DITA (<http://dita.xml.org/>) are important formats for single source publishing
- DocBook was developed as a book-oriented document type
- DITA is a topic-oriented alternative that is based on the principle of didactic minimalism

## Office formats
- Microsoft Office and Libre Office/Open Office use XML as native format
- Office Open XML is a (controversial) ECMA standard (<http://www.ecma-international.org/publications/standards/Ecma-376.htm>)
- The Open Document Format (<https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office>) is XML based and an OASIS standard
- Libre Office also supports DocBook

## Markup languages
- Basis: SGML, developed since the 1960s
- HTML was developed as an SGML application
- XML emerged in the 1990s as an alternative to HTML and a simplified version of SGML
- HTML5 prevailed over XHTML as the living HTML standard.
- At the same time JSON established itself as a simple format for data exchange on the Web

## Transformation and presentation
- XML allows a strict separation of content and presentation
- XML documents are usually converted with XSLT into other XML vocabularies or HTML
- XSLT is a functional programming language that uses XML syntax
XSL-FO was developed for page-oriented output

## Microdata
- As microdata, machine-readable information can be embedded in HTML documents (https://www.w3.org/TR/microdata/)
- RFFa and Jason are alternatives
- Microformats have a similar objective, but are based on older HTML mechanisms
- We recommend the orientation to Schema.org

## RDF/RDFa
- RDF is a standard for semantic information on the Web
- RDF can be serialized as XML, but also in other formats
- RDF was developed as a basic technology for the Semantic Web
- With RDFa, RDF data can be embedded in HTML documents
- The Open Graph Protocol (http://ogp.me/) developed by Facebook is based on RDFa

## Resources
- [Extensible Markup Language (XML)](https://www.w3.org/XML/ "Extensible Markup Language (XML)")
- [XML.com](https://www.xml.com/ "XML.com")
- [data2type GmbH: XML Technologies | Reference Book](https://www.data2type.de/xml-xslt-xslfo/ "data2type GmbH: XML Technologies | Reference Book")
- [xml \@ZVON.org](http://zvon.org/comp/m/xml.html "xml @ZVON.org")

# XML syntax

## XML syntax
- angle brackets distinguish markup and text content
- Most important syntactic features: elements, attributes, comments
- Well-formed XML follows syntactical rules: Elements are closed and embedded in each other, attributes have values in quotation marks, and upper and lower case are case sensitive.
- Valid XML corresponds to a defined document type

## Example of an XML document

```xml
<?xml version="1.0"?>
<!-- dictionary.xml
 - Copyright (c) 2014, HerongYang.com, All Rights Reserved.
-->
<dictionary>
 <word acronym="true">
  <name>XML</name>
  <definition reference="Herong&apos;s Notes">eXtensible Markup
Language.</definition>
  <update date="2002-12-23"/>
 </word>
 <word symbol="true">
  <name>&lt;</name>
  <definition>Mathematical symbol representing the "less than" logical
operation, like: 1&lt;2.</definition>
  <definition>Reserved symbol in XML to representing the beginning of
tags, like: <! [CDATA[<p>Hello world!</p>]]>
  </definition>
</word>
</dictionary>
```

## XML declaration


```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
```

- Stands at the beginning of a document, indicates the XML version.
- Optional: Specifies the encoding (character encoding)
- Optional: specification of the referencing of an external document type declaration (DTD)

## comments

```xml
<!-- dictionary.xml
 - Copyright (c) 2014, HerongYang.com, All Rights Reserved.
-->
```

- Contain messages for human users
- Are not used by the XML processing software


## Document element

```xml
<dictionary>
.
.
.
</dictionary>
```

- Each XML document has one and only one root element
- No tree structure could be built without a root element

## Attribute

```xml
<word acronym="true">
.
.
.
</word>
```

- Elements and attributes are the most important syntactical components of XML documents
- Elements can have a content, attributes have a *value*
- The sequence is relevant for elements, but not for attributes


## Elements

```xml
<name>XML</name>
.
.
.
<update date="2002-12-23"/>
```

- Start and end tag
- Element names
- Empty elements

## Attributes

```xml
<update date="2002-12-23"/>
```

- Attribute names and attribute value
- values are always enclosed in quotation marks
- Order of the element is not relevant

## Empty elements

```xml
<update date="2002-12-23"/>
```

- Shortened syntax: Slash before the Closing Bracket

## Entites

```xml
Herong&apos;s Notes"

..., like: 1&lt;2

```

- For special characters
- For the representation of characters that would otherwise be interpreted as markup


## CDATA sections

```xml
<definition>Reserved symbol in XML to representing the beginning of
tags, like: <! [CDATA[<p>Hello world!</p>]]>
  </definition>
```

- For sections that should not be interpreted as markup.
- Example: HTML within RSS documents


## Further examples


- [A List Apart: Using XML : Sample XML Document](https://alistapart.com/article/usingxml/ "A List Apart: Using XML : Sample XML Document")

- [Sample XML File (books.xml)](https://msdn.microsoft.com/en-us/library/ms762271(v=vs.85) "Sample XML File (books.xml)")



## Text editors

Online: [Online XML Editor](https://www.tutorialspoint.com/online_xml_editor.htm "Online XML Editor")

## Encoding

- Representation of characters by bits and bytes
- ASCII and Friends: 1 character - 1 bit
- Unicode: 1 numeric value per character in each writing system
- Unicode encodings: Conversion of numerical values into bytes



## Syntax Highlighting

## Validating Editors
[Vervollständigung mit dem nxml-Modus des Emacs](pics/nxmlmode-completion.png){ Breite=80% }

(Befehl: `C-M-i`)


## Online tools

[W3C XML-Schema (XSD) validation online](http://www.utilities-online.info/xsdvalidation/#.WenM6hN-qRs "W3C XML-Schema (XSD)-Validierung online")

[Free Online XML Validator] (https://www.liquid-technologies.com/online-relaxng-validator "Kostenloser Online-XML-Validator (RelaxNG)" (Relax NG)

[XSLT (eXtensible Stylesheet Language Transformations) Online-Transformationen](http://www.utilities-online.info/xsltransformation/#.WenPLRN-qRs "XSLT (eXtensible Stylesheet Language Transformations)
