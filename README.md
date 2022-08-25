# Differential Equations - An Introduction for Engineers

A free online textbook for a first course in differential equations.  See https://sites.rutgers.edu/matthew-charnley/course-materials/differential-equations-an-introduction-for-engineers/. This book was created with the *Notes on Diffy Qs* text by Jiri Lebl as a starting point. This book has some additional content and was reordered to fit the class that is normally run. See https://www.jirka.org/diffyqs/ for information on that text. 

## Branches:

* ``master`` branch is the current working version, version 0.9.

## Files

* ``ENGODE_Book.tex`` is the main file, no real content here, that's in the chapter files
* ``chap-*.tex`` are the files with the content of the various chapters, also minimal content here, most is in the section files. Appendices are also included as chapters (matlab-intro and prereq, for instance)
* ``chap-*/sec-*.tex`` contain the information from each section within the chapters.
* ``bookFormat.sty`` is the preamble for the PDF version
* ``mywrapfig.sty`` is a slightly modified wrapfig.sty (fixing intextsep nonsense)

* Figures are in ``figures/``

The shell(``.sh``) and Perl(``.pl``) scripts here are mostly really hacky ways to just do things.  Feel free to ignore them. These were untouched from Jiri Lebl's Notes on Diffy Qs. For this text, there is currently no web version available (yet). 

* ``runpdf.sh`` does a thorough job of compiling the source to a pdf
* ``getstats.sh`` gets statistics about the current version like number of exercises, and such.
* ``convert-to-mbx.*`` is work in progress conversion script to PreTeXt (used to be MathBookXML or MBX) for a better looking online version.  The output is not plain PreTeXt, it contains custom elements.  The script to run is ``convert-to-mbx.sh``, which is a shell script.  This runs ``convert-to-mbx.pl`` which actually does the conversion, then it runs ``xsltproc`` on the result.  The result is stored in ``html`` subdirectory (old one is moved out of the way).  Some svg and png figures are created in the process, they can be optimized by ``optimize-svgs.sh`` (uses ``svgo`` which you might have to install) and ``optimize-pngs.sh``.  Currently uses the svgs by default with pngs as fallbacks.  Notice that ``svgo`` currently clobbers some of the more complicated figures without disabeling one of the plugins.  So best to check the output for correctness.  There is a flag ``--full`` for doing the entire conversion and optimization.
* ``fixup-html-file.pl``: a perl script invoked in the web version generation.
* ``pdftopng.sh`` is a script to convert a pdf figure to a png.
* ``resizepdftocrownquatro.sh`` is a script to resize a pdf into a crown quatro size paper.

## Notes

The tex sources require a very recent LaTeX, if your latex does not have a recent enough ocgx2 package, you can simply comment out that line in ``diffyqssetup.sty``.

## Extra Files

At this point, there are many files here that came from *Notes on Diffy Qs* that are not included in the text. Several chapters have been omitted from the text and may be included at a later time. They are included here for consistency and continuity. 

## Old Files

The ``old-sec`` folder contains previous section files, either original or from *Notes on Diffy Qs*, that were omitted as a part of this text development. Again, there are here for continuity. 
