## Chapter 2 - The Nature of Complexity

### 2.1 Complexity Defined
***Complexity*** is anything related to the *structure* of a software system that makes it hard to understand and modify the system.

Isolating complexity in a place where it will never be seen is almost as good as eliminating the complexity entirely

Your job as a developer is not just to create code that you can work with easily, but to create code that others can also work with easily.

### 2.2 Symptoms of Complexity
#### 1. Change Amplification
When a seemingly simple change requires code modifications in many different places. For example, a website defines the background color for each webpage explicitly vs defining the background color in a central place where each web page can reference it.

#### 2. Cognitive Load
How much a developer needs to know in order to complete a task. For example, a C function that allocates memory, returns a pointer to that memory, and then ***assumes*** the caller will free that memory. In this case, the developer needs to know that they are responsible for freeing the memory after using the function.

Sometimes an approach that requires more lines of code is actually simpler, because it reduces cognitive load.

#### 3. Unknown Unknowns
When it is not obvious which pieces of code must be modified to complete a task, or what information a developer must have to carry out the task successfully. For example, a website defines the background color for web pages centrally, but a few pages use a darker shade defined explicitly in the individual pages. Developers are unlikely to realize this, so they may change the central color and not the other colors to match.

This symptom is *the worst of the three*. There is something you need to know, but there is no way for you to find out what it is or even whether there is an issue. You won't find out until bugs appear after you make a change.

One of the most important goals of good design is for a system to be ***obvious***

### 2.3 Causes of Complexity
Complexity is caused by two things: ***dependencies and obscurity***

Dependencies are a fundamental part of software development and can't be completely eliminated. One of the goals of software design is to **reduce the number of dependencies** and to make the **dependencies that remain as simple and obvious as possible**.

In many cases, obscurity comes about because of inadequate documentation. However, obscurity is also a design issue. If a system has a clean and obvious design, then it will need less documenation.

The best way to reduce obscurity is by ***simplifying the system design***

### 2.4 Complexity is Incremental
The incremental nature of complexity makes it hard to control. And once complexity has accumulated, it is hard to elimnate since fixing a single dependency or obscurity will not, by itself, make a big difference.

In order to slow the growth of complexity, you must take a ***zero tolerance approach***
