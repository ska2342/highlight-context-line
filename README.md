# Highlight Context Line

A minor mode for Emacs to improve orientation when scrolling.

[![Melpa Status](http://melpa.org/packages/highlight-context-line-badge.svg)](http://melpa.org/#/highlight-context-line)

## Context Line

The line of your Emacs buffer that is at the top of the window before
you start to scroll, is considered the context line. It is the last
line in the view after scrolling that was visible before
scrolling. Similarly the line at the bottom of the window is the
context line for scrolling down.

When enabled, this minor mode just highlights the context line. On the
next keypress the highlight is removed.

## That sounds weird. Just show me.

![Animated GIF showing the effect](https://raw.githubusercontent.com/ska2342/highlight-context-line/master/highlight-context-line-demo.gif)

## Inspiration

Back then when the first version of this little minor mode was
written, `gv` was a good reader for postscript files. Whenever you
scrolled it painted a line across the document that reflected where
the previous view ended. I found that useful and wanted it in Emacs,
too.

## On the web

Canonical page http://www.skamphausen.de/cgi-bin/ska/highlight-context-line

## Compatibility

This is only tested with Gnu Emacs >24. I don't think it works in
other flavors of Emacs.

If you prefer XEmacs, try the version 1.5 (initial state of this repo)
which I originally wrote on XEmacs. It may still work and does mostly
the same.

# Installation

## MELPA

This available on MELPA. So you can install it via Emacs' package
manager.

* See http://melpa.org for how to setup MELP if you havn't already.
* `M-x package-install highlight-context-line RET`

## Manual

* Clone this repo
* Add the new directory to your `load-path`
* `(require 'highlight-context-line)`

## Enable the Minor Mode

* To test, run `M-x highlight-context-line-mode` repeatedly to turn it
  on or off.
* To enable permanently, add to your init file

```elisp
(highlight-context-line-mode 1)
```

# Customization

There is really just one thing to customize: the face that is used to
highlight the context line: `highlight-context-line-face`.

Note: For me, setting it to `:underline` does not draw the underline
to the (right) edge of the window while some background color does. 
