# EQ-SANS reduction map (drtsans)

**Page: https://cw-do.github.io/eqsans-drtsans/**

A map of what [drtsans](https://github.com/neutrons/drtsans) does to EQ-SANS data, from neutron events
to I(Q) and I(Qx,Qy).

- Each row is a run (sample, sample transmission, empty beam, background transmission, background).
- Each column is an operation, in the order drtsans applies it.
- A stop exists only where that operation is applied to that run, and lines merge where data are combined.
- Press Play, or click any stop: the panel below shows what the data look like there, and the card
  lists the function, source file and line that does it, with the JSON keys that control it.

Open `#s11` at the end of the address to land on stop 11.

## What is real and what is illustrative

- **Real:** the order of operations, which run gets which operation, the functions, files and line
  numbers, and the formulas. They were read from `neutrons/drtsans`, branch `next`, commit `0e34b07`
  (2026-11-20); every code link on the page is pinned to that commit.
- **Illustrative:** every number in the data animations. They come from a small toy reduction
  (48 × 64 pixels, 16 wavelength bins, a made-up sample) that runs the same arithmetic in the same
  order in your browser. No measured data are in this repository.

This is not official drtsans documentation. If the code has moved on, the code is right.

## Files

`index.html` is a single self-contained page (no build step, no dependencies). It is generated from a
working copy kept elsewhere, so changes made here by hand will be overwritten.
