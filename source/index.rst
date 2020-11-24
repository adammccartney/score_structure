A brief overview of a possible score structure
==============================================

Learning how to develop a score using abjad remains one of the more
challenging aspects for new users. While it is possible to generate
some interesting music fragments using abjad through an interactive
prompt, and possible to create full scores from a concise single script,
it's not at all obvious how one might go about structuring a larger project
that allows for the structuring of musical information into a score and parts.

What this page aims to do is to provide a simple, high-level description
of a score structure, offer some very basic guidance on what each subdirectory
could contain and go on to recommend a few useful resources that handle aspects
of software development in more detail.

What this page does not aim to do is to give a step by step tutorial on
creating scores with abjad, to give a detailed description of class functionality
within the individual submodules in a score package or to explain the details of
python packaging.


```
~/Scores/example/example
├── builds
├── distribution
├── etc
├── __init__.py
├── Makefile
├── materials
├── segments
├── stylesheets
├── test
└── tools
```


Persistence, Modules and Packages
=================================

In many of the examples contained in the abjad documentation the interactive prompt
is used to generate short musical fragments to briefly demonstrate some feature.
The process of working with scores is by nature quite different, it is by nature
based around iteration and incremental improvement rather than simply "finding
the right formula". So how do iteration and incremental improvement work in terms
of abjad? Well, basically abjad is excellent and generating lilypond code and one
of the main ways that persistence is handled is in the form of lilypond source files.
The generation of such files will be covered in more detail in the section on segments. 

While a thorough understanding of python modules and packages won't necessarily tell you
anything about musical scores, they are pretty much essential for understanding how the
individual components within a score package interact. The python standard documentation
and Mark Lutz's introductory python book are two good places to start. 

Creativity
==========

Chapter 5 of Josiah Wolf Oberholzer's 2015 dissertation is titled "Composition as software development"
and contains a much more detailed look at some of the same information contained in this document. 
Specifically, he provides detailed examples of how he has structured the contents of a score
package in relation to his own compositional work. 

An important thing to remember when working with software development is that a well written
program creates a very accurate model of a set of ideas. In essence, this is similar to
what a well written score does, it provides a clear, abstract representation of a composition,
which itself is simply a collection of musical ideas.

While it is beneficial to spend time studying source code listings of existing score examples
and reverse engineering them in order to figure out how they work, it is probably much more
beneficial to spend time imagining the type of musical ideas that you want to represent
with a score. 


.. toctree::

   :maxdepth: 2
   :caption: Contents:

   builds
   distribution
   etc
   Makefile
   materials
   segments
   stylesheets
   test
   tools



