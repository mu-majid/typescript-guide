## Overview

  * This repository includes notes/projects for typescript.

  ### 1-syntax-and-features:

  * The first directory has some examples on  TS features and syntax like interfaces, types, ...

  ### 2-maps:
  * The maps directory is a PoC on the importance of interfaces and why we need them. In this project two markers on a google map are shown to indicate the route between a user and his/her company. This project relies on `parcel-bundler` for running TS in the browser.

  ### 3-sort
  * The sort directory contains code for a simple sorter that takes array, string, or a linked list and sorts it. Also in this project reusability is in mind and how to write generic code. The main idea from this project is that we need to apply the same set of steps/instructions (bubble sorting) on different data structures (number[], string, linkedList). Interfaces are important here.
  * Interfaces and Abstract Classes differences: *Always try to stick to interfaces when possible*
  ![interface-vs-abstract-class](./img/inter-vs-abst.png)

  ### 4-stats:
  * The stats directory is a project that reads football.csv file containing football matches results and analyze these data, then generate a report for it. In this project code-reuse is done via two way (CSVReader and MatchReader Entites) -> First one is through inheritance and abstract classes, and the other is via composition and interfaces.
  * Generics are introduced in this projects
  ![generics](./img/generic.png)
  * this project has two implementation for the CSV and Match Reader -> Inheritance and compoaition.
  * *Favor object comppsition over class inheritance* is the most misundertood statement in the javascript comunity. In this statement, composition means using interfaces and the `has a` relation between objects insead of the `is a` relation between classes. This usually done via delegation.
  * In javascript, people normally refer to object composition as uing Object.assign for example. Which is basically inheritance.

  ### 5-web:
  * This project is a front-end web framework (like React) that has basic features (like handling events, rendering content, and saving/retrieving data) that will help you build front-end components. The project basically has two main folders, Models and Views. Models is for fetching, saving, and interacting with data. And Views is about what is shown on the browser to the user.
  * In this project I used `Extraction Approach` which means, Build a mega class (with tons of functionality) representing an Entity -> Then refactor that Entity class using composition -> Then Refactor The Entity class to be reusable class and represent any piece of data, not just a specific Entity.
  * The Entity was a User class that had three main functionalities: 
  1) Ability to save/retrieve user data on a remote server.
  2) Listen to events on a user instance, and trigger event handlers associated with these events.
  3) Create a user with feeding the class some Attributes
  * These three functionalities were extracted into three separate classes, and interated into User class via composition, so that, when any functionality is needed -> delegation to the responsible class occurs.
  