## Overview

  * This repository includes notes/projects for typescript.
  * The first directory has some examples on  TS features and syntax like interfaces, types, ...
  * The maps directory is a PoC on the importance of interfaces and why we need them. In this project two markers on a google map are shown to indicate the route between a user and his/her company. This project relies on `parcel-bundler` for running TS in the browser.
  * The sort directory contains code for a simple sorter that takes array, string, or a linked list and sorts it. Also in this project reusability is in mind and how to write generic code. The main idea from this project is that we need to apply the same set of steps/instructions (bubble sorting) on different data structures (number[], string, linkedList). Interfaces are important here.
  * Interfaces and Abstract Classes differences: *Always try to stick to interfaces when possible*
  ![interface-vs-abstract-class](./img/inter-vs-abst.png)
  * The stats directory is a project that reads football.csv file containing football matches results and analyze these data, then generate a report for it.
  