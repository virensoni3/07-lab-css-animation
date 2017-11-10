# Lab 05: CSS animation 01

A simple CSS animation demo with four stages.

View the [GitHub page for this example](https://ctec3905.github.io/05-lab-css-animation/).

Note that animation makes processor demands, which are of special concern on mobile devices:

good
: 'transform' uses a RenderLayer so the GPU calculates the position
: works for translate, scale, rotate, opacity

bad
: 'position' triggers 'layout' so the CPU must recalculate each frame
: *never* use for mobiles or with "animation-iteration: infinite;"

So only use animations for simple once-only user interaction cues (e.g. on hover) or to attract attention with a repeating animation that is triggered by some user action (e.g. by adding a class to show a missing form field, or moving a button to suggest clicking).