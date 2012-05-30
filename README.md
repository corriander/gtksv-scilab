gtksv-scilab
============

Scilab syntax highlighting via GtkSourceView 3 (used by programs such as gedit). 

This repo houses an attempt to achieve two goals: 

	- Emulate SciNotes 1.1 default highlighting behaviour as closely as possible.
	- Provide an alternative, toned down, interpretation of the default schema.

Please note that this has been developed on gedit 3.2.3. It should work in other
contexts (other gedit versions or other GtkSV3-enabled applications) but it's 
not been tested (yet). Functionality in GtkSV2 (e.g. gedit 2.x) is unknown.

Current status
--------------

scilab.lang is in a working state
scinotes.xml is a WIP
scilab.xml is TODO

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

Your installation may vary.
