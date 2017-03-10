# Highlight Context Line

A minor mode for Emacs to improve orientation when scrolling.

## Context Line

The line of your Emacs buffer that is at the top of the window before
you start to scroll, is considered the context line. It is the last
line in the view after scrolling that was visible before
scrolling. Similarly the line at the bottom of the window is the
context line for scrolling down.

When enabled, this minor mode just highlights the context line. On the
next keypress the highlight is removed.

## Inspiration

Back then when the first version of this little minor mode was
written, `gv` was a good reader for postscript files. Whenever you
scrolled it painted a line across the document that reflected where
the previous view ended. I found that useful and wanted it in Emacs,
too.

## Compatibility

This is only tested with Gnu Emacs >24. I don't think it works in
other flavors of Emacs.

If you prefer XEmacs, try the version 1.5 (initial state of this repo)
which I originally wrote on XEmacs. It may still work and does mostly
the same.

# Installation

## Manual

* Clone this repo
* Add the new directory to your `load-path`
* `(require 'highlight-context-line)`

# Customization

There is really just one thing to customize: the face that is used to
highlight the context line: `highlight-context-line-face`.

Note: For me, setting it to `:underline` does not draw the underline
to the (right) edge of the window while some background color does. 
