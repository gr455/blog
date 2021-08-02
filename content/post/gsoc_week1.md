---
title: "GSoC Week 1: The Beginning"
date: 2021-06-15T18:24:22+05:30
draft: false
featured_image: "/img/gsoc.png"
---


I was selected for the Google Summer of Code '21 with [CircuitVerse](https://circuitverse.org) this year and this blog post and the ones following this will document my journey through the program.

[CircuitVerse](https://circuitverse.org) is a Digital Logic Simulator on web. It is an educational tool for students interested in electronics to simulate and make circuits on their browser. It also has features for professors to give assignments and grades.

My project is to implement a testbench to automatically test circuits against test cases. This will replace the existing testbench element in favor of more robust testbench which runs faster, supports sequential circuits and gives the user greater control over running tests.

## Community Bonding Period

I had been contributing to CircuitVerse since September 2020, so I was familiar with the community. Still the community bonding period was a blast! I got to meet the entire core development team at CircuitVerse and all the other GSoC students over a video conference. My mentors were extremely welcoming and helpful too.
I discussed the goals and features of the testbench project with **Satvik Ramaprasad** and **Dr. Richard Pawson** and decided on the flow from the user point of view.

I also read a lot of code during this period (I am half decent at reading code from all that I have read while auditing for security stuff). Since my project is very close to the simulator engine, I had to be familiar with the working of the engine. Reading all this code really made me appreciate CircuitVerse. It takes Data Structures and Algorithms and integrates them seemlessly into a working product.

## Coding | Week 1 (June 7 - 13)

The first week of coding, my goal was to make the user interface for creating tests. These tests could further be used with the testbench. CircuitVerse already had a very crude UI present to achieve this, but it was not user friendly and didn't fit with the new testbench design anyway, so I had to start from scratch and rewrite the testbench creator.

It went from this

![Old Test Creator](/blog/img/tbc_old.png)

To this (excuse my bad CSS skills in some places)

![New Test Creator](/blog/img/tbc_new.png)

To complete this quickly, I put all the code for the UI into one ruby view. This will need to be changed. I will split the styles, scripts and even make partial views wherever necessary.

Apart from this, I started work on the backend for the tests, and was in the process of implementing CRUD operations when my mentor told me that it's best that the backend is left at the end as a feature and to finish up work on the engine first. This was my fault. I should have communicated my status better with the mentor. That would have enabled me to work on engine earlier rather than working on the backend. So for now, the backend is on a pause (will finish that after the engine is done and the testbench works) and the coming week will be spent implementing the engine.

Overall, the first few weeks of GSoC have been really fun, and I'm sure it only gets better from here :D
