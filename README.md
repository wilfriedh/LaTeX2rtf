latex2rtf is a translator program that translates LaTeX text into the
RTF format used by various text processors, most notably Word.

For the Copyright of the Program see the file Copyright.

Version 2.3.18 resolves "latex2rtf ignores '-C'" 
   (Michael Artmann 2018-09-08),
adds support for user defined counters accessed through 
   \the<counter> (Pedro Andres Aranda Gutierrez 2018-12-28),
cleans up Makefile, isolating DESTDIR from PREFIX 
   (Pedro Andres Aranda Gutierrez 2018-12-28),
adds hebrew.cfg

Version 2.3.17 adds support for non-ascii characters in verbatim blocks
and theorem captions (Alex Itkes 2018-03-14) 
and support for the proof environment  (Alex Itkes 2018-03-19)

To install (on a UNIX system)
     On modern Linux distributions, you would prefer to install
     LaTeX2RTF by the package manager of your distribution, which also
     provides an easy means for update and uninstallation.
     If your package manager does not provide the LaTeX2RTF package or
     you need to install LaTeX2RTF from the sources for some other
     reason, you should consider using 'checkinstall' which creates a
     package for your package manager which then can be installed and
     uninstalled by the package manager.

     If you nevertheless need to run install from the sources, note the following:
     If your 'mkdir' doesn't support the '-p' option, then create the
     necessary directories by hand and remove the option from the
     '$MKDIR' variable.  If you have other problems, just copy
     'latex2rtf' and 'latex2png' to a binary directory, and move the
     contents of the 'cfg/' directory to the location specified by
     '$CFG_INSTALL'.

- Edit Makefile for your local configuration.  The default install
  is reasonable, but if you do not have root access, then you might
  need to set $DESTDIR to be your home directory.
- make
- If this is not your first-time installation, you may want to preserve
  your old configuration (*.cfg) files. Copy them to a safe place before
  installing.
- [sudo] make install

- make check   (expect warnings but no errors)
     [OPTIONAL] This tests LaTeX2RTF on a variety of LaTeX files.
     Expect a whole lot of warnings, but no outright errors.  (On IBM
     AIX, use 'gmake check'.)  Note that this will check the basic
     functionality of the 'latex2png' script, and then that of
     'latex2rtf'.
