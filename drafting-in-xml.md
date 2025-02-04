---
title: Drafting in XML
description: 
published: true
date: 2021-11-16T09:16:11.563Z
tags: 
editor: markdown
dateCreated: 2021-08-18T10:56:56.326Z
---

# Introducing RFCXML
For an introduction to RFCXML see the [RFCXML overview and background](/rfcxml-overview) and for detailed documentation on each element and attribute see the [RFCXML vocabulary reference](/rfcxml-vocabulary).

# What to look for in an XML toolchain
There are two key features to look for in an XML toolchain:
1. RNC schema validation. This ensures that your document is valid RFC XML as you type it.
1. RNC aware editing support. 

To take advantage of these features your XML code must include an [`<?xml-model ...>`](https://www.w3.org/TR/xml-model/) processing instruction as found in [Templates and schemas](/templates-and-schemas).

# RFC XML toolchains
The following XML toolchains have been reported as in use by IETF community members.  These are all interactive XML editors. 

## 1. Emacs editor in nXML Mode
The popular open source editor Emacs includes [nXML Mode](https://www.gnu.org/software/emacs/manual/html_mono/nxml-mode.html), which enables validation and schema-sensitive editing when you use an RNC schema. 

## 2. Other text editors
IETF community members report using a range of text editors some of which provide specific support for XML editing and some of which don't, and validating the RFCXML externally.

## 3. Commercial XML Editors
The one commercial XML editor that we are aware of people using is [Oxygen XML Editor](https://www.oxygenxml.com/xml_editor.html).  This tool comes in different versions with a number of different licensing options, though all versions support RELAX NG validation and some support syntax highlighting and intelligent auto-completion. The premium version also supports collaborative edIting, including tracked changes and comment review.

The same company also makes [Oxygen Content Fusion](https://www.oxygenxml.com/content_fusion.html), which support web-based collaborative editing and document review.
  
## 4. XMLmind XML Editor (XXE) with xml2rfc-xxe
[XMLmind XML Editor (XXE)](https://www.xmlmind.com/xmleditor/) is a commercial near-WYSIWYG XML editor with a free edition for personal use.  XXE supports RNC schema validation and context-sensitive editing.

A community developed configuration for XXE, [xml2rfc-xxe](https://github.com/wkumari/xml2rfc-xxe/) is available, providing additional context-sensitive editing features, however this does not support the latest version of RFCXML and is unsupported.

# Supporting tools
Authors writing in XML may find the following tools helpful:

## 1. Add XML tags for RFC2119 keywords
This [script](https://strayalpha.com/software/rfcxml/lookback-bcp-fix.pl) adds `<bcp14>` tags around RFC 2119 keywords in XML source.

## 2. bibtex2rfc
[bibtex2rfc](https://github.com/yaronf/bibtex2rfc) converts BibTeX citations into BibXML references. The IETF publishes a [library of BibXML references](https://xml2rfc.tools.ietf.org), which should be checked first.
