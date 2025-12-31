# Unit 3 : Software Design

### Importance of Design

- Design is a meaningful engineering representation of something that is to be built. It can be traced to a customer‘s requirements.
- Design focuses on four areas which are data, architecture, interfaces and components.
- The design in software engineering plays important role without that if we start developing product then it will be confusion making, error prone, components at wrong place. In nut shell computer software is complex in nature than a house, so we need a design as a blueprint.

### Design Principles

- The design process should not suffer from tunnel vision. A good designer should
consider alternative approaches, judging each based on requirements of the problem,
the resources available to do the job, and the design concepts.
- The design should be traceable to the analysis model. Because a single element of
design model often traces to multiple requirements of the problem, it is necessary to
have a means for tracking how requirements have been satisfied by the design
model.
- The design should not reinvent the wheel. Systems are constructed using a set of
design patterns, many of which have likely been encountered before. These patterns
should always be chosen as an alternative to reinvention. Time is short and resources
are limited. Design time should be in representing truly new ideas and integrating
those patterns that already exist.
- The design should be structured to accommodate change. The design concepts
discussed in the next section enable a design to achieve its principle.
- The design should be structured to degrade tenderly, even when aberrant data ,
events or operating conditions arises. Properly designed software should never
explode. It should be designed to house unusual conditions, and if it must terminate
processing, do so in a polished manner.
- Coding means not design. Design means not coding. When in depth procedural
designs are created for program components, the level of abstraction of the design
model is higher as compare to source code. The only design decisions made at the
coding level address the small implementations details that enable the procedural
design to be coded.
- The design should be assessed for quality as it is being created not after fact. A
variety of design concepts and design measures are available to assist the designer in
assessing quality.

### Module Level Concepts

- Modular design has become accepted approach in all engineering disciplines. A modular design reduces difficulty, facilitates change and results in easier implementation.
- Software is divided into separately named and addressable components, called modules.
- **Effective Modular Design :**
    - **Functional Independence :** The concept of functional independence is a direct outcome of modularity and the concepts of abstraction and information hiding.
    - Functional independence is achieved by developing modules with sole minded function and an aversion (dislike) to excessive interaction with other modules.
    - That means we want to design software so that each module addresses a specific sub function of requirement and has a simple interface when viewed from other parts of the program structure.

### Cohesion & Coupling

- Independence is measured using two qualitative criteria :
    - **Cohesion :**  refers to the degree to which elements within a module work together to fulfill a single, well-defined purpose. High cohesion means that elements are closely related and focused on a single purpose, while low cohesion means that elements are loosely related and serve multiple purposes.
        - At the low end of the cohesion we come across a module which performs a certain set of tasks that relates to each other loosely. Such modules are termed coincidently cohesive.
        - Modules performs tasks so as to are related logically is logically cohesive.
        - When a module contains tasks so as to are related by the fact that all must be executed with the same span of time, the module exhibits temporal cohesion.
        
        ![Cohesion-(1)-1024.webp](Unit%203%20Software%20Design/Cohesion-(1)-1024.webp)
        
    - **Coupling :** refers to the degree of interdependence between software modules. High coupling means that modules are closely connected and changes in one module may affect other modules. Low coupling means that modules are independent, and changes in one module have little impact on other modules.
        
        ![coupling-(1)-1024.webp](Unit%203%20Software%20Design/coupling-(1)-1024.webp)
        

### Interface Design

- **Screen Design :** The screen design should be visually appealing. It should be simple and neat. Web pages use dazzling colors and lots of images to make them attractive, this type of design takes a longer time to load the pages.