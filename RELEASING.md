# Release process checklist

To release a new version of xword-dl for flathub:

* Make a new branch
* Update puzzle-sets-xword-dl first. Make sure that the
  `python-requirements.json` file there is updated from upstream.
* Copy `python-requirements.json` into this directory. It should be
  identical.
* Update `xword-dl` wrapper script to point to the new PYTHONPATH directory.
* Update flathub manifest to include new git tags for
  puzzle-set-xword-dl and xword-dl.
* **Build the flatpak locally!** It's very possible to break things
  between the puzzle-set-xword-dl flatpak and this one.
* Push to flathub and open a merge request
