# Unofficial Guide to Modding Project Zomboid

This document will focus on explaining the methodology used to create, publish and install Project Zomboid modifications. The goal of this guide is to provide, as considered by author, the best way to create, publish and install Project Zomboid modifications. What is implied by *best way* is explained later in the guide.

This document is intended to be a complete guide that guides you through the process of modding various game aspects, providing detailed examples and explaining the reasoning behind the methodology used. If you are just looking for references, tutorials, code examples or a quick guide to creating simple modifications you should read [Project Zomboid Modding Guide](https://github.com/FWolfe/Zomboid-Modding-Guide) instead which serves more as an unofficial Project Zomboid wiki.

## Disclaimer

Readers are encouraged to remember that all information in this guide is presented as *opinion* as opposed to *fact*. Any information directing readers to do one thing instead of another is intended to be taken as *advice* as opposed to an *order*. Proposed methodology should not be taken as a *critique* of personal nature, in order to advance the nature of anything a healthy dose of criticism is needed. The author of this document does not assume **responsibility** or give **warranties** of any kind. This includes responsibility for offended sensibilities, mood swings, sleepless nights or damage to your software or hardware. The author of this document also make **no guarantee** that any and all information in this guide is accurate at any time beyond the point at which it was written.

Readers should note that the methodology proposed in this guide is not presented as the *only way*, but rather the *best way* of modding Project Zomboid. Readers should also be aware that the methodology proposed in this guide is currently **not accepted** as the recommended way of modding Project Zomboid. This makes it more difficult to find documentation and support from community channels when using said methodology.

## Motivation

The process of game modding is a fun and rewarding activity where players get to modify the game to create interesting and engaging content for themselves and others to enjoy. It can also be exhausting, time consuming and mind numbing experience with most time being spent on preforming tedious tasks, searching for documentation and solving unexpected problems. Not using the right tools, looking at the right places, or learning the right things all lead to frustration and an eventual burnout. The primary purpose of this guide is to make your modding experience more fun and less tedious.

## Requirements

- Patience and dedication to learn how to create and publish modifications the right way.
- Willingness to adopt open source software development workflows and principles.
- Basic knowledge of creating content which the readers wants to modify the game with. For example, if the reader wanted to learn how to implement a new or modify an existing 3D model in the game, the guide would assume the reader is capable of creating or modifying the model on his own and would instead focus on explaining the procedure of preparing the model and importing it in the game.

In addition to the requirements listed above the following knowledge is recommended but not required:

- Previous knowledge of Project Zomboid or game modding in general. Having previous knowledge of game modding will make the guide much easier to follow, however the guide will explain modding methodology by assuming the reader has no previous experience modding Project Zomboid or any other game. Note that some aspects of the guide are intended for modders with intermediate and advanced modding experience and will be marked as such.
- Basic knowledge of software development principles and practices. This is recommended because the reasoning behind much of the methodology proposed will be easier to understand for those with some experience in developing software. However, the guide will explain the development principles and practice by assuming the reader has no previous knowledge of said principles and practices.

