# LSBD Seminar web page

## About 

This repo is the [Jekyll][jekyll] source to the LSBD 
seminar's web page.

## Documentation

New talks and terms can be added without editing either 
`index.html` or `past-terms.html`.  Here are some details 
about configuration and new data.

### Configuration

This happens in `_config.yml`.  The main attribute here is `seminar_current_term`,
which needs to be updated to the tag of the current term when this changes.

Right now, we have "Fall", "Spring", and "Summer" terms.  (These are not exactly Aalto teaching periods, but the fouding organizers have no idea what these are.)

### Terms

This file `_data/seminarterms.yml` contains a list with entries of the form

~~~~~~~~~~~~~~
- 
    tag: spring2016
    name: "Spring 2016"
~~~~~~~~~~~~~~

When the term changes, add the new term in the same form.  The `tag` attribute is used in the top-matter of talk files.  The `name` attribute is used to generate the 
list of talks from past terms.

### Talks

Each talk is in its own file in the directory `_seminartalks`.  The file name should be of the form `YYYY-MM-DD-LASTNAME.md`.  (This guarantees correct sorting.)

The files have a header with the following form:

~~~~~~~~~~~~~~
---
layout: seminartalk
speaker: Kalle Kytölä
speakerinst: Aalto University
speakershortinst: Aalto
speakerurl: https://math.aalto.fi/~kkytola/
talktitle:  Scaling limit correlations for planar loop-erased random walks and uniform spanning trees
talkdate: 05.04.2016
talktime: 16.15
talkplace: AScI lounge (TUAS 3161)
talkterm: spring2016
title: "Large Structures Seminar - Kalle Kytölä"
dinnerplace: 
dinnertime: 
dinnerurl: 
---
~~~~~~~~~~~~~~

When the term changes, switch the `talkterm` attribute to the new one.

We usually use `DD.MM.YYYY` as the date format.

The body of the file is the talk abstract.  This is Markdown format with MathJax that is basically the same as what you have on MathOverflow, except that all formulas are delimited by `$$`, and it's inline unless it is in its own paragraph.
