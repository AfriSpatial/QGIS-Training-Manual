About the Project
=================

This manual was originally produced by Linfiniti Consulting CC
(http://linfiniti.com) and is now a community effort.

Contributions
=============

Make sure that you understand and agree to the license conditions for this
project before contributing.

To edit the source
------------------

To add content to the (English) source, you will need:

* Git version control software. Refer to git's documentation for help.
* A local clone of the manual's `repository
  <https://github.com/qgis/QGIS-Training-Manual>`_. You may wish to work on
  your own fork of this repository and submit a pull request later.
* The latest stable installation of `QGIS <http://qgis.org/>`_ software (in
  which to produce examples).
* A basic text editor to edit the RST text files which contain the content.
  Take care not to commit Windows line endings!
* A method to make and edit screenshots. When adding screenshots, put them in
  the "_static_en" directory. Use the existing structure as an example.

To edit existing translations
-----------------------------

* You'll need a translation editor such as `Qt Linguist
  <http://code.google.com/p/qtlinguistdownload/>`_ or `Virtaal
  <http://translate.sourceforge.net/wiki/virtaal/index>`_. Use it to edit the
  .po files for your language, found under the i18n folder.
* When creating new screenshots, always save them under the same name as the
  ones they are to replace. If you use your own file names, the images won't
  show up in the document.

To add new translations
-----------------------

* The languages that will be considered for translation are in the
  "pre_translate.sh" and "post_translate.sh" scripts.
* In order to create a fully functional translation for a language, open each
  of these scripts and edit their LOCALE lists.
* Add the two-letter code for your chosen language to all of the LOCALE lists
  and save the files.
* Run the "pre_translate.sh" script.

To render documentation
-----------------------

* Run the "post_translate.sh" script.
* You may add the two-letter language code of your language as a parameter to
  make the script only render documentation for the language you specified.
* The output directory is _build, which is not under version control.
* Alternatively, to render the English documentation only as html, run the
  command "make html".
* The English PDF render target is specified by using "make latexpdf".
* You may need to install "texlive" or "texlive-full" for PDF rendering to
  work.

Theming
-------

To use the theme, run the command "git submodule update --init
linfiniti-sphinx-theme" to load the theme submodule from git.
