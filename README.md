nerlim
======

An updated Master Bibliography File for use with custom-bib

To use it, you need to have P. W. Daly's `custom-bib` package installed. It is part of TeXLive, but if you don't have it, it's available at http://www.ctan.org/pkg/custom-bib. The `makebst` script enables you to generate a BibTeX bibliography style file (.bst file) according to a large number of possible customization options. See the `custom-bib` documentation for details on how this works.

The file `nerlim.mbs` is derived from `merlin.mbs` ver. 4.33. When you run 

    latex makebst

you will be given a lot of questions for how you want your bibliographies to look.  In the end, you're left with a .dbj file, which you then run through `latex` to generate a new, custom bibliography style .bst file for use with BibTeX. In this process, just use `nerlim.mbs` instead of `merlin.mbs` when asked.

`nerlim.mbs` will generate .bst files that differ from `merlin.mbs`-derived .bst files as follows:

 - volume numbers are attached to journal titles by a tie, not a space.
 - there's an option to indicate multiple occurrences of the same author by whatever `\bibdash` produces.
 - a `book` with both an author and an editor will not produce an error, but instead will give the editor(s) after the title, in the same format as `incollection` and `inproceedings` editors are formatted.

Included in this repository also:

 - `opencourt.dbj`, a batch file to generate a .bst file according to Open Court specs.
 - `opencourt.bst`, said .bst, generated by running `latex opencourt.dbj`
 - `opencourt.bib`, a test bibliography file
 - `opencourt.tex`, a test LaTeX file
