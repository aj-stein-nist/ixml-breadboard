
# iXML Breadboard

Various experiments and tools for iXML, [Invisible XML](https://invisiblexml.org), aiming for full support for iXML-defined formats within XSLT-based projects.

Here at the top level you will find tooling, configuration and documentation.

This work builds on a foundation laid by members of the iXML and XML communities.

## Maturity and maintenance plan

Use at your own risk. Because this constitutes primary development work whose main intent is to provide examples for borrowing, it comes without warranty or explicit maintenance plan.

The idea is to maintain the site in an "as is" state, useful for itself. Feel free to copy its code elsewhere or take inspiration, while crediting your sources as always.

## Testing iXML

In addition to the utilities provided and documented in this repository, these are invaluable utilities for testing iXML:

- Steve Pemberton's [Run ixml](https://homepages.cwi.nl/~steven/ixml/tutorial/run.html) iXML processor (runs on CWI server)
- John Lumley's [iXML Workbench](https://johnlumley.github.io/jwiXML.xhtml) based on his [jωiXML Processor](https://github.com/johnlumley/jwiXML) ("Joey" - runs in your browser)

## Reading about iXML

- [Invisible XML](https://invisiblexml.org/) community landing page maintains many links including (or jump to)
  - [Invisible XML Specification](https://invisiblexml.org/1.0/) version 1.0
  - Steven Pemberton’s [hands-on tutorial](http://www.cwi.nl/~steven/ixml/tutorial/)
  - Other tutorials and intro treatments including from Norm Tovey-Walsh

## How to Do It

Start by browsing the repository to survey its contents and state.

### iXML examples

In the [`ixml`](ixml/) directory are several samples of iXML grammars (applications) at various stages of progress. These can also be tested using external utilities such as  [iXML Workbench](https://johnlumley.github.io/jwiXML.xhtml).

https://github.com/invisibleXML/ixml/tree/master/samples also gives some examples from community members.

### Scripted routines supporting batch (standalone) processing

(*Planned*)

For guidance on available scripts, see the [`src` directory readme file](src/readme.md).

### Applications in the browser

Wherever an HTML file appears, typically an application can be served from a plain vanilla web server.

For example, in file `index.html` this directory provides a "workbench" application for testing an iXML parse. To run it:

- Start a web server (Apache, Node.js http-server or your preference) from this directory (i.e. using it as root), e.g.
  - open a command prompt
  - start `http-server`
- Using a current browser, open `http://localhost:8080/index.html`
- Examine and test the application

When started at the root of the project, a web server can also serve any file in the project, subject to its configuration, and different experiments may offer different entry points.

## Dependencies

### Browser applications

The browser applications generally rely on two libraries for Invisible XML and XSLT 3.0 respectively:

-  [jωiXML](https://github.com/johnlumley/jwiXML) SaxonJS application by John Lumley, with a test application, the [iXML Workbench](https://johnlumley.github.io/jwiXML.xhtml)
- [SaxonJS](https://saxonica.com/saxon-js/index.xml), by Michael Kay and Saxonica [Saxonica](https://saxonica.com/welcome/welcome.xml)

These are used and deployed in accordance with [their licenses](THIRD_PARTY_LICENSES.md).

### Scripts

These scripts and libraries rely on `bash`, Maven, XML Calabash, Saxon, and components for Calabash as documented for iXML. These are all open source (while components may be experimental / in development).

Install [Maven](https://maven.apache.org) to manage software dependencies; check for or install [`bash`](https://www.gnu.org/software/bash/) to run invocation scripts.

Many thanks to the developers of all layers in this impressive commodity stack!

- [XML Calabash](https://xmlcalabash.com/) and [NineML]() - Norm Tovey-Walsh
- [Saxon](https://saxonica.com/welcome/welcome.xml) - Mike Kay and associates
- [XML](https://www.w3.org/XML/) and [XSLT](https://www.w3.org/Style/XSL/)
- Java, open-source operating systems, network protocols ...

## Project planning

Planned:

- Landing page with links to online tools and guidance (this page)
- Working grammars 
- in-browser iXML Breadboard based on jwiXML
  - application-specific SaxonJS processors 
- CL support via XML Calabash and CoffeePot coffee.nineml.org
  - end to end
  - iXML parsing as in-Saxon function call (sacks.nineml.org)
  - 'grammar compiler' producing a portable XSLT module for any grammar?
- XSpec testing harness for parsers
- Resource kit for experimenting
  may be PoCs for other projects
  - NGAC
  - XPath 3.0
  - Metapath (port from ANTLR)
  - LMNL syntax? (in my branch :-)

Goals:

- Knowledge and command of grammars (specifically iXML grammars) as a way of specifying and processing inputs
- iXML tools support
  - XProc (following Norm TW)
  Plugin support for any iXML grammar into an XProc pipeline
  both as (primary or ) inputs
  and embedded (function calls)
  validation and error reporting support
- functionalities in application
  - Metapath
  - NGAC?


## Contact information

Principal Investigator: Wendell Piez, NIST (US National Institute of Standards and Technology) ITL/CSD (Information Technology Laboratory, Computer Security Division).

Email w e n d e l l (dot) p i e z (at) n i s t (dot) g o v.

## README (retained from template)

Each repository will contain a plain-text [README file][wk-rdm],
preferably formatted using [GitHub-flavored Markdown][gh-mdn] and
named `README.md` (this file) or `README`.

Per the [GitHub ROB][gh-rob] and [NIST Suborder 1801.02][nist-s-1801-02],
your README should contain:

1. Software or Data description
   - Statements of purpose and maturity
   - Description of the repository contents
   - Technical installation instructions, including operating
     system or software dependencies
1. Contact information
   - PI name, NIST OU, Division, and Group names
   - Contact email address at NIST
   - Details of mailing lists, chatrooms, and discussion forums,
     where applicable
1. Related Material
   - URL for associated project on the NIST website or other Department
     of Commerce page, if available
   - References to user guides if stored outside of GitHub
1. Directions on appropriate citation with example text
1. References to any included non-public domain software modules,
   and additional license language if needed, *e.g.* [BSD][li-bsd],
   [GPL][li-gpl], or [MIT][li-mit]

The more detailed your README, the more likely our colleagues
around the world are to find it through a Web search. For general
advice on writing a helpful README, please review
[*Making Readmes Readable*][18f-guide] from 18F and Cornell's
[*Guide to Writing README-style Metadata*][cornell-meta].
