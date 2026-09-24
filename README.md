# mobile-market-data

What the Omarchy Mobile **Market** app knows about each plugin from the
[Omarchy plugin market](https://omarchyplugins.com) that it can't get from
the market itself: how well the plugin works on a phone, and what it looks
like there.

It's produced by an automated test run that installs each overlay and panel
plugin on the phone's shell (in a VM at 360×780), opens it, taps through it,
and screenshots every screen it reaches.

- `verdicts.json`: one entry per plugin, keyed by market id: the commit that
  was tested, a rating (`perfect`, `usable`, `desktop only`, `not usable`,
  `broken`, or `retest` for one whose screenshots were taken at the wrong
  screen size and has not been tested again yet), notes in plain words, what it needs (camera, API key…), and the
  file names below.
- `shots/<id>-<n>-<hash>.webp`: up to three phone screens.
- `icons/<id>-<hash>.webp`: a square cut from the top of the first screen.

File names carry a hash of their content, so a plugin that is re-tested and
looks different gets new names.

Generated. Don't edit by hand: changes are overwritten by the next run.
