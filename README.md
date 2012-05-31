gtksv-scilab
============

Scilab syntax highlighting for GtkSourceView enabled programs (e.g. gedit). 

This repo houses an attempt to achieve two goals: 

1. Emulate SciNotes 1.1 default highlighting behaviour as closely as possible.
2. Provide an alternative, toned down interpretation of the default schema.

Please note that this has been developed on gedit 3.2.3. It should work in other
contexts (other gedit versions or other GtkSV3-enabled applications) but it's 
not been tested (yet). Functionality in GtkSV2 (e.g. gedit 2.x) is unknown.

Current status
--------------

- scilab.lang is the language specification and is essential. It should 
work in conjunction with arbitrary colour schemes, but in order to get
scinotes-like highlighting it must be used in conjunction with scinotes.xml.
The vast majority (probably) of keywords/macros/primitives shipped with 
Scilab 5.3.3 should be recognised. Semantic highlighting is not possible
with GtkSV3 as far as I know, so there are no externally defined functions,
user variables or macros.

- scinotes.xml is the scinotes colour/style specification and has been
written to take advantage of the syntax specification in scilab.lang to 
emulate the SciNotes 1.1 styles as closely as possible. A major focus has been
on making this a template style file as colour schemes are very personal 
and whilst this is aimed at a very specific "scheme" (a strong word) I 
intend to adapt it later so I've tried to make it easy and clear to 
customise or base other styles on.

scilab.lang is in a working state

scilab.xml is TODO

tl;dr 

scilab.lang contains the Scilab 5.3.3 syntax spec, scinotes.xml has a 
SciNotes 1.1 colour scheme (for use with scilab.lang) and is optional. The 
value of the colour scheme for non-scilab syntax is ..debatable. 

Installation
------------

Highlighting in GtkSV-utilising applications is dependent on two distinct 
elements; a language specification file and a style file which dictates the 
styles referred to in the language specs.

GtkSV language specs (*.lang) reside in a folder 
	
	path/gtksourceview-3.0/language-specs/ 

Style files (*.xml) reside in 

	path/gtksourceview-3.0/styles/ 

On Ubuntu 11.10

	path=/usr/share

OR (on a per-user basis, folder and subfolders can be created if not present)

	path=/home/<username>/.local/share

Your installation may vary, but just drop the files in the right folder.
