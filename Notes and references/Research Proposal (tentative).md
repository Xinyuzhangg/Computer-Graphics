# Research Proposal (tentative)



## 1. Research Statement

We want to research on the physics based simulation of the objects falling down and the following shattering and fracturing effects. 

In computer graphics, physics based simulation and rendering is one of the most attractive and challenging topics, in this research we want to approximate the real to life effects in fracturing with the least price in calculation. Generally speaking, we want to come up with a lifelike simulation on the shattering of objects and optimize the simulation with more resonable physics and test it with different materials and geometric shapes. 

Firstly, we plan to make a simplification and start with 2D. It's going to be a square, triangle or sphere made up by glass material and falling to the solid ground and then fracturing into 2D fragments, so the physics is much simpler and we can tell if we have applied the right equations.

Secondly, we are going to simulate in 3D space and adapt the model and its characteristics from 2D to 3D

In the end, if our primitive model is sucessful, we can change into different materials and geometric shapes. For example. the glass cup can be switched to a ceramic cup to observe the physical difference between glass material and ceramic material.



## 2. Background and Rationale 

We have learned that physics based simulation can be achieved with many methods, among which are mass-spring system method, finite element method, and particle system method. These methods all have their advantages and disadvantages. For example, using particle systems to simulate the shattering and fracturing of object is hard because the calculation of a large number of particles is expensive and time consuming[^1][^2], and it's difficult to predict the physics model promptly and accurately. There isn't a simulation which can both perfectly fit the physics model and do real-time simulation yet. And our choice of methods requires some serious comparison and justification.

As the physics engine develops and new programming languages emerge, we are provided with more efficient data structure[^3] and new analytical models[^4] , so that we expect to make the simulation of motion, colliding and shattering of different geometries and materials to be more real to life and faster to calculate. We are very excited to combine the most advanced computer graphics progress and see what we can achieve.



## 3. Team Members and Advisor

***Advisor***

* **Professor Carlo Sequin**

***Team Members***

* **Xinyu Zhang** -- **(coordinator)**
  Specialize in modeling, physics analysis and graphics rendering

* **Peter Generao**
  Specialize in mathemitical calculation and analysis
* **Yuyue Wang**
  Specialize in system compiling, debugging and algorithm optimization
* **Juhan Jin**
  Specialize in coding and system programming



## 4. Timeline

### 4.1 General Research Time Length

* **From July to October** 
  We estimate that the four of us can be dedicated to the research full time and achieve our basic simulation model and code framwork
* **Since October**
  After the beginning of the new semester, we expect to take as much available time as possible to do the modification, rectification and optimization until we have a scientificly rigorous and theoretically satisfying result.

### 4.2 Research Phase

#### *Early Period*

* Physics background analysis and mathematical calculation
* Model optimization and feasibility analysis
* Geometry modeling

#### *Middle Period*

* Coordination of the project progress
* Contribution to code
* Contribution to the paper 

#### *Late Period*

* Result optimization
* Debugging
* Result visualization and animation

### 4.3 Regular Team Events Meeting 

#### *Weekly*

* Report progress to the advisor and make a summary via zoom/mail

#### *Daily* 

* Log the daily progress and task completion status

* Task distribution and update
* Team meeting via zoom and group chat

#### *Irregular*

* Meeting and Solving the problems and difficulties each individual meets and seek for the help of the advisor if necessary



## 5. Developming Environment

**languages**: C++, Python

**Tools and APIs**: OpenGL, ARCSim, Taichi

**Modeling**: Blender



## 6. Website and Link

We have set up a GitHub repo to serve the collaboration and update our progress <https://github.com/Xinyuzhangg/Computer-Graphics.git>



## 7. References

[^1]: James F. O'Brien and Jessica K. Hodgins. "Graphical Modeling and Animation of Brittle Fracture". In Proceedings of ACM SIGGRAPH 1999, pages 137–146. ACM Press/Addison-Wesley Publishing Co., August 1999.

[^2]: Smith, Jeffrey, Andrew Witkin, and David Baraff. "Fast and controllable simulation of the shattering of brittle objects." Computer Graphics Forum. Vol. 20. No. 2. Oxford, UK and Boston, USA: Blackwell Publishers Ltd, 2001.

[^3]: Yuanming Hu, Luke Anderson, Tzu-Mao Li, Qi Sun, Nathan Carr, Jonathan Ragan-Kelley, Frédo Durand: “DiffTaichi: Differentiable Programming for Physical Simulation”, 2019.

[^4]: Tobias Pfaff, Rahul Narain, Juan Miguel de Joya, and James F. O'Brien. "Adaptive Tearing and Cracking of Thin Sheets". ACM Transactions on Graphics, 33(4):xx:1–9, July 2014. To be presented at SIGGRAPH 2014, Vancouver.
