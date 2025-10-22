# Release process checklist

To release a new version of xword-dl for flathub:

* Make a new branch
* Create an updated `python3-xword-dl.json` command by running:
  `flatpak-builder-tools/pip/flatpak-pip-generator --runtime='org.gnome.Sdk//48' xword-dl`
* Add "-I" to the pip command in the generated json file. This will
  tell it to ignore the versions of the python files that crosswords
  uses for the convertor.
* If the python version has changed, update `xword-dl` wrapper script
  to point to the new PYTHONPATH directory,
* Update flathub manifest to include new git tags for
  puzzle-set-xword-dl, if they've changed.
* **Build the flatpak locally!** It's very possible to break things.
* Push to flathub and open a merge request
