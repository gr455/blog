---
title: "GSoC Week 6, 7: Engine refactor and UI Improvements"
date: 2021-08-05T18:24:22+05:30
draft: false
featured_image: "/img/gsoc.png"
---

## Coding | Week 6 (July 17 - 23)

This week I had planned to work on data part of the tests. Since we had decided for test data to be a part of the circuit data, that is what I started implementing. I had to change the save and load functions of circuits to also save and load the test data.

Apart from this, I also made some UI changes to make the UI more responsive and added a `loadData` function to the test creator, so that users can load the JSON data back to the creator to modify it.

Finally I made the UI themes compatible. CircuitVerse has a couple themes that you can switch between, I introduced some css variables instead of hardcoding colors to make the UI theme compatible.

This is how the testbench looks in a dark theme.
![Testbench with Dark Theme](/blog/img/tb_darkmode.png)

## Coding | Week 7 (July 24 - 31)

This week I refactored the engine code and made a class out of the testData. I felt this was required because the test data handling was not trivial and was better off abstracted away in a class. Furthermore, my mentor also suggested me the same.

There were also multiple issues with the testbench UI and data handing which I solved this week.

Some of the issues I fixed include:

 - Update Testbench UI on creation of new circuit
 - Fix Testbench JSON dialog font color not matching the theme
 - Remove Testbench creator extra whitespace in identifiers
 - Hide Testbench UI from layout mode
 - Fix copy pasting removes testbench data from scope
 - Fix showing validation error causes circuit to block

 Here's a [link](https://github.com/CircuitVerse/CircuitVerse/pull/2366) to that PR.

The upcoming weeks, we are discussing the best ways to include the creator with the testbench (since right now they are seperate entities) so that it is easier for user to create and load tests.


