---
title: "GSoC Week 2, 3: The Engine"
date: 2021-06-28T18:24:22+05:30
draft: false
featured_image: "/img/gsoc.png"
---

This is the second installment in my blog series on Google Summer of Code 2021 with [CircuitVerse](https://circuitverse.org)

## Coding | Week 2 (June 14 - 20)

This week I had planned to focus on the testbench engine.
Me and Satvik (the Mentor for this project) decided that the engine should consist of two modes:

 - RUNALL mode: In this mode, all the tests are run without any user interaction. For this, the engine takes control of the clock so that the speed is not limited by the clock time. The engine ticks the clock once all the input values are propagated through the entire circuit (instead of relying on clock time). Rendering of the circuit is also disabled to increase the speed of testing.

 - MANUAL mode: In this mode, the user is given an interface where they can choose which test to run. The chosen test is run similar to RUNALL mode, except now the circuit is also rendered.

I wrote the functions that would be used by the testbench to run. The main parts of the engine were:

 - An interface function that will be called when the testbench has to be run
 - A main function for both (RUNALL and MANUAL) modes
 - Helper functions

## Coding | Week 3 (June 21 - 27)

This week, I planned on finishing up the testbench entirely (except for the backend). The only thing left to do was to finish up the Test Creater UI and Make a UI for the MANUAL mode.

I finally finished up the UI design for both of these and started doing final cleanup and trying to satisfy CodeClimate (the code linter we use on CircuitVerse). Frustrated by some of the ESLint rules, I opened up a discussion on some of the linting rules on the CircuitVerse Slack Channel😂.

Finally, I had done some tangible work. I could see the testbench working and it felt amazing to be able to see my work in action.

![New Test Creator](/blog/img/manual_mode_ui.png)

Finally, I satisfied ESLint as much as I could and made a [PR](https://github.com/CircuitVerse/CircuitVerse/pull/2289).

For the upcoming weeks, I will be focussing on creating the backend for the tests. For all this time, I was manually copy-pasting the JSON containing test data. Hopefully, by the end of first evaluation, backend will be finished.