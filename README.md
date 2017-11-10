# Lab 05: CSS animation 01

A simple CSS animation demo with four stages.

View the [GitHub page for this example](https://ctec3905.github.io/05-lab-css-animation/).

Note that animation makes processor demands, which are of special concern on mobile devices:

## Good practice

- the CSS `transform` property uses a RenderLayer so the **GPU** can do the calculations
- works for CSS `transform` property values: `translate`, `scale`, `rotate`, `opacity`

## Bad practice

- other properties need a more extensive screen redraw and 'trigger layout'
- browser 'layout' forces the **CPU** to recalculate every frame
- *never* animate other properties for mobiles or with `animation-iteration: infinite;`

So only use animations for simple once-only user interaction cues (e.g. on hover) or to attract attention with a repeating animation that is triggered by some user action (e.g. by adding a class to show a missing form field, or moving a button to suggest clicking).

See: [High Performance Animations](https://www.html5rocks.com/en/tutorials/speed/high-performance-animations/) (HTML5 Rocks, 2013)