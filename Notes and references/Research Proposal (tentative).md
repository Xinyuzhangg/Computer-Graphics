# Research Proposal (tentative)

## Research Statement

> What specific question will you pursue with your research and why is it important to the field? This section enables you to give the reviewers an overview of your project. Keep in mind that other sections give you an opportunity to develop more details around the background, methodology, and rationale for the project.

We want to research on the computer graphics simulation of the objects falling down and the following shattering and fracturing of the object. 

In computer graphics, physics based simulation and rendering is one of the most attractive and challenging topics, in this research we want to approximate the real effects in fracturing with the least price in calculation. Generally speaking, we want to come up with a true to life simulation on the shattering of objects and optimize the rendering with faster speed and test it with different materials and geometric shapes.

## Background and Rationale

> What is already known about the field of research you will be working on? How does your research project fit in with what is being done currently in the field, and how does it build upon knowledge on the topic or fill in gaps in the field? Please cite references from the literature when applicable; these citations should be listed in #5 of this proposal. 

Simulating the shattering and fracturing of object is hard because the calculation of a large number of particles is expensive and time consuming[^1][^2], and it's difficult to predict the physics model promptly and accurately. There isn't a simulation which can both perfectly fit the physics model and do real-time rendering yet.

As the physics engine develops, new programming languages provide us with more efficient data structure[^3] and new analytical models[^4] emerge, we expect the simulation of motion, colliding and shattering of different geometries and materials to be more real to life and faster to calculate. We are very excited to combine the most advanced computer graphics progress and see what we can achieve.

## Timeline

July - October

> Please define the main challenges of your project and what research methods you will use to address these challenges. Describe your research plan for the summer in chronological order - either use a week-by-week timeline or phases approach (i.e. week 1, week 2…or phase 1, phase 2…). Each week/phase should specify goals, action items, and methods. Please include in your plan information about exactly how/when you will check in with your research mentor.

## Tools and Programming Languages

Coding languages: c++, python

Tools and APIs: openGL, ARCSim, Taichi

## Team Members

***Advisor***

* Professor Carlo Sequin

***Team Members***

* Peter Generao

* Yuyue Wang

* Xinyu Zhang

* Juhan Jin

## Task Distribution

***Early Period***

* Physics background analysis and mathematical calculation
* Model optimization and feasibility analysis
* Geometry modeling

***Middle Period***

* Coordination of the project progress
* Contribution to code
* Contribution to the paper 

***Late Period***

* Result optimization
* Debugging
* Result visualization and animation

## References

[^1]: James F. O'Brien and Jessica K. Hodgins. "Graphical Modeling and Animation of Brittle Fracture". In Proceedings of ACM SIGGRAPH 1999, pages 137–146. ACM Press/Addison-Wesley Publishing Co., August 1999.

[^2]: Smith, Jeffrey, Andrew Witkin, and David Baraff. "Fast and controllable simulation of the shattering of brittle objects." Computer Graphics Forum. Vol. 20. No. 2. Oxford, UK and Boston, USA: Blackwell Publishers Ltd, 2001.

[^3]: Yuanming Hu, Luke Anderson, Tzu-Mao Li, Qi Sun, Nathan Carr, Jonathan Ragan-Kelley, Frédo Durand: “DiffTaichi: Differentiable Programming for Physical Simulation”, 2019.

[^4]: Tobias Pfaff, Rahul Narain, Juan Miguel de Joya, and James F. O'Brien. "Adaptive Tearing and Cracking of Thin Sheets". ACM Transactions on Graphics, 33(4):xx:1–9, July 2014. To be presented at SIGGRAPH 2014, Vancouver.
