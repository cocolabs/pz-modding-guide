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

## Methodology

Before we explain the different modding aspects, it is important to understand the proper methodology used to create and publish mods. The methodology proposed here should be adhered to regardless of what aspects of modding you are engaged in. As explained in the [Motivation](#motivation) section, our primary motivation should be to have fun by create interesting content. In order to consistently create mods and keep motivated we have to adhere to sane workflows.

### Reasoning

The proposed methodology consists of advanced tools and workflows. Learning to apply this methodology to your modding process takes time and dedication. Here are some of the common reasons mod developers give for not using advanced tools and workflows:

- They are not getting paid for creating mods, it is only a hobby.
- They do not need all the features provided by advanced tools and workflows.
- They do not have the time to install and learn how to use advanced tools and workflows.

On the surface these reasons might feel perfectly reasonable, but let's take a closer look at each argument.

The first argument claims that **there is no need to put care and effort into something that is only a hobby**. Take for example any major open source project that is widely used by countless users on a daily basis, like Linux projects. Linux is free software and as such does not make any money from sales. Most contributors to Linux projects do not get paid and are not looking to get paid. Their main motivation is not money. If the Linux community did not want to put effort into supporting the projects because *it's only a hobby and they are not getting paid for it*, Linux would not be what it is today.

The second argument claims that **since not all features of the tool are needed, using the tool makes little sense**. If we think about all the advanced tools we use in out day to day life we can easily think of numerous examples of tools that offer a lot more features then what we are currently using. Take for example your mobile phone. This is an advanced tool that you are only partially utilizing because you don't need to use the countless features this devices has to offer, yet you are still using it. It is clear that it offers benefits that other more simplistic contraptions (such as rocks and shoestring cups) cannot match.

The third argument claims that **the time needed to install and learn how to use advanced tools does not justify it's benefit**. This argument comes from not knowing the actual benefit of said tools and workflows. If you thought that the benefit of driving a car over traveling around the world on a horse is negligible you would never buy a car and live the rest of your life as a true cowboy. The main benefits of using the methodology proposed in this guide is increased efficiency which leads to overall higher mod quality and more enjoyable workflow which brings more motivation used to create amazing mods.

### Design



### Version control

In this section we are going to explain what version control systems (VCS) are, how to use them, and why they are an integral part in any modding process. Always remember that game modding is just downscaled game development and is thus not excluded from software development practices.

#### What is VCS?

Here is a good summary of what version control is:

> Version control, also known as source control, is the practice of tracking and managing changes to software code. Version control systems are software tools that help software teams manage changes to source code over time. Version control software keeps track of every modification to the code in a special kind of database. If a mistake is made, developers can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption to all team members. It is important to state that version control is not just used to version code. It should be used on any project file that can be versioned, which includes text files, model files, image files etc.

Read more about version control in this [article](https://www.atlassian.com/git/tutorials/what-is-version-control), after which you should know everything you needed to get started with version control.

#### Why use VCS?

The main question you might be wondering is why you should use such a seemingly complex system in your modding workflow. In addition to everything already said in the article linked above the answer is simple: **it benefits the whole community**.

When you are using version control in your project and hosting it on a repository hosting service such as [Github](https://www.github.com) you are leaving a complete long-term change history of every file contained within your project. This means every change made by you and potentially other individuals you collaborated with over the complete lifespan of development is recorded in detail. When you eventually stop developing the project it can be easily picked up by other developers and continually developed until they pass the torch to others. Introducing version control in your modding workflow helps the community by making your development process cleaner, more readable and easier to understand and follow.

Imagine if every mod project you ever came across used version control. How many outdated and abandoned mods have you seen and wanted to revive but had no idea where to begin? How many active mods struggle with simple bugs authors are unable or unwilling to resolve due to *spaghetti* code which makes them more and more reluctant to continue development with each line of code they write? The reason for this is that the authors did not keep a clean record of what they were doing. Most modders will say that code documentation is important but very few will admit that documenting project changes is equally important.

#### How to use VCS?

The most widely used modern version control system in the world today is [Git](https://www.atlassian.com/git/tutorials/what-is-git). When using Git every developer's working copy of the code is also a repository that can contain the full history of all changes. This ensures that your project, along with a detail record of of changes, is always safe as long as a single copy of your project repository is present somewhere, which should always be the case as long as you are using a repository hosting service. The recommended repository hosting service is [Github](https://www.github.com) due to it's great support for open source projects, intuitive web-interface and easy project management.

- Start by [installing](https://www.atlassian.com/git/tutorials/install-git) Git. It is easy to install and as with most software the installation process depends on your operating system.
- In addition to installing Git it is also recommended to install [Github Desktop](https://desktop.github.com/) (see [here](https://github.com/shiftkey/desktop) for Linux version). It is a Git desktop client which makes using Git much easier by providing a clean user interface that keeps simple Git tasks simple and provides much needed quality of life.
- Once you have Git installed read [git - the simple guide](https://rogerdudler.github.io/git-guide/) to learn the basics of using Git.
- Download or bookmark these cheat sheets to help you out when you forget Git commands:
  - [Atlassian Git Cheat Sheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet).
  - [Simple Git Cheat Sheet by Roger Dudler](https://rogerdudler.github.io/git-guide/files/git_cheat_sheet.pdf).
  - [Git command references by yooksi](https://gist.github.com/yooksi/913a23562063ed1925d8064cb9ba35b3).

Learning how to use version control is a long but worthwhile process. Mod developers have to start using version control in their mod development workflows to help improve the quality of mods and provide better community support for new modders.

### Documentation

Every mod project should contain documentation that clearly states how to use and configure the mod. If there are special installation steps needed to make the mod work those should be documented as well. This documentation should be written in a `README` file that should reside in the project root directory.

In addition to this, if the mod project contains code, the code itself should be sufficiently documented as to allow others to easily study and understand the code.  It should also allow other developers to continue developing the project without getting in contact with the original author.

#### Project wiki

Larger projects are encouraged to open and maintain a wiki page where they can document different project aspects in detail. For example; a mod that expands foraging should have a wiki page that lists all the different plants that can be foraged, a mod that adds more cooking recipe should list those recipes along with recipe schematics that inform the players how to use them, a mod that overhauls zombies behavior should split each behavior category in different pages and provide a detailed explanation of how exactly do different aspects of behavior differ from vanilla behavior.

The recommended way of creating and hosting wikis is with [Github wikis](https://docs.github.com/en/communities/documenting-your-project-with-wikis/about-wikis). It allows you to write pages in Markdown and HTLM format. It also allows others to contribute either directly or via pull requests, since each wiki is a Git repository with it's own detailed history of changes.

### Licensing

The final and most important aspect of modding methodology is licensing. Developing mods is a fun activity that most of us do for fun, however this reason should not preclude ethical considerations. Mods should always be developed and distributed under ethical principles.

As mentioned in the previous section, the main reason for learning and practicing version control is to help the modding community. In turn the modding community helps you. Nobody knows everything and the value of collective knowledge always outweighs that of individual knowledge.

For this same reason mod developers should keep their mods open source (since version control does not benefit the community if it is kept secret) and allow users essential freedoms when using their mods. Keeping your project open source means that the source code and asset project files are open for anyone to use, study and modify. This principle allows other people to contribute to the development and improvement of mods like a community.

As stated by [GNU](https://www.gnu.org/philosophy/free-sw.html) free and open source software should give users the following essential freedoms:

> - The freedom to run the program as you wish, for any purpose.
> - The freedom to study how the program works, and change it so it does your computing as you wish.
> - The freedom to redistribute copies so you can help others.
> - The freedom to distribute copies of your modified versions to others.

Many mod developers are hesitant to make their projects open source as they are afraid that by doing so they are allowing others to steal their work and claim it as their own. This stems from a fundamental misunderstanding of what *free software* is. When declaring your project open source you are not telling the world that you forgo all legal rights and that anyone can do what they want with your work. You are telling the world that they **have the freedom to run, copy, distribute, study, change and improve** your work, nothing more. Most open source licenses protect your work under threat of legal punishment against actions such as someone taking your work and publishing it under his name.

Before starting a mod project you should think about [choosing an open source license](https://choosealicense.com/) that works best for you. The best choice for small and simple projects is the [MIT License](https://choosealicense.com/licenses/mit/) which lets people do almost anything they want with your project, like making and distributing closed source versions. However, if you are working on a more serious project I would recommend the [GNU GPL v3](https://choosealicense.com/licenses/gpl-3.0/) license which also lets people do almost anything they want with your project, *except* distributing closed source versions. Not allowing people to distribute closed source versions helps enforce the principles of free software.

When uploading your mod to the [Steam Workshop](https://steamcommunity.com/workshop/) you grant Valve the following rights:

> Right to use, reproduce, modify, create derivative works from, distribute, transmit, transcode, translate, broadcast, and otherwise  communicate, and publicly display and publicly perform, your User  Generated Content, and derivative works of your User Generated Content, for the purpose of the operation, distribution, incorporation as part of and promotion of the Steam service, Steam games or other Steam offerings, including Subscriptions. This license is granted to Valve as the content is uploaded on Steam for the entire duration of the intellectual property rights.

The excerpt above was taken from the [Steam Subscriber Agreement](https://store.steampowered.com/subscriber_agreement/#6). Many believe that by uploading to the Steam Workshop you grant Valve complete ownership and intellectual property rights to your work. After reading the linked subscriber agreement you can see that this is simply not true. You are irrevocably granting valve certain rights for the duration of the intellectual property rights, but you still retain full intellectual property rights and Valve is not able to take those rights away from you. They are however able to exercise the rights you gave them for the full duration of the agreement.

## Tools

Here is a list of essential tools that every mod developer should use:

- [Notepad++](https://notepad-plus-plus.org/) - Free source code editor and Notepad replacement written in C++. It should be preferred over programs like Atom and Sublime due to it's efficiency and simplicity. It is a very **portable** yet **powerful** tool that allows for advanced text manipulation and formatting. You can use it's expansive search functionality to find text occurrences in files across different directories (recursively) from a single search action. It also support searching, marking and replacing text with regular expression. With that and a lot more advanced features at your disposal Notepad++ is your most efficient tool for searching, editing and formatting text. Note that this only applies to text, when writing code your preferred tool should always be IntelliJ IDEA.
- [IntelliJ IDEA](https://www.jetbrains.com/idea/) - Integrated development environment written in Java for developing software. It allows you to read, write, decompile and search through game code. It also allows you to efficiently search through game scripts and other text based files with an easy to use user interface that supports search scopes and regular expressions. It is also used to setup your **mod development environment**, which is the primary reason it is recommended as an essential tool for all mod developers. Read more about setting up you development environment in [Environment](#environment) section. In addition to this it is important to note that this is the same program used by **The Indie Stone** developers to write game code.

## Environment

Setting up your mod development environment is the first step in creating your first mod.

Properly installed mod development environment will allow you to do the following from the comfort of your IDE:

- Easily setup correct mod structure and assemble mod distribution.
- Easily decompile and read game code with code navigation support.
- Write Lua code with an up-to-date API documentation attached to project.
- Launch and debug Project Zomboid with console logging and use of breakpoints.
- Fully automate changelog generation and create mod distributions with a click of a button.

Developers that write code will benefit from following features in their IDE:

- Code analysis helps spot bugs and avoid lengthy debugging sessions.
- Code navigation helps quickly find what we are looking for saving us time and energy.

Since the development environment includes many interconnecting systems which need to be configured in the right order, it is difficult to setup manually. This is why [The Storm Project](https://github.com/pzstorm/) has created [Capsid](https://github.com/pzstorm/capsid). It is a [Gradle](https://gradle.org/) plugin that enables powerful IDE features and improves your modding workflow. It helps automate the  process of setting up, assembling and deploying your project. Read the project [`README`](https://github.com/pzstorm/capsid/blob/master/README.md) for information on how to install, configure and use Capsid.

## Writing code

Project Zomboid's codebase is divided into two main components; the *frontend* and *backend*. The frontend is written in Lua and is mainly focused on defining the user interface. The backed is written in Java and handles most of game logic, rendering objects, registering user input and much more. 

Since the early days of Project Zomboid there was only ever two ways of modding the game; with Lua using the official API or with Java by modifying and recompiling game Java classes. The following sections list the advantages and disadvantages of both approaches.

### Lua modding

Official modding support is implemented with modified [Kahlua](https://code.google.com/archive/p/kahlua/), a Lua interpreter written in Java. It reads instructions written in Lua and executes them with Java Virtual Machine. Lua interacts with Java using an [API](https://projectzomboid.com/modding/) defined in [LuaManager](https://projectzomboid.com/modding/zombie/Lua/LuaManager.html). Methods defined in [LuaManager.GlobalObject](https://projectzomboid.com/modding/zombie/Lua/LuaManager.GlobalObject.html) are exported as global Lua functions and classes exported by `LuaManager.Exposer` are available as global Lua tables. 

#### Advantages

- Easy to learn and write mods with.
- Has officially supported API.
- Supported by the modding community. 

#### Disadvantages

- Unable to access classes and members that are not directly exposed by API.
- No type safety or on-the-fly compiler errors makes it more difficult to write code. 
- More difficult to debug due to lack of proper debugging tools.
- No control over memory management.

#### Limitations

- Does not implement all standard Lua modules such as `io.*` and `os.*`.
- Java classes that have not been directly exposed by `LuaManager.Exposed` are not accessible from Lua.
- Java class fields are not accessible from Lua regardless of whether the owner class is directly exposed or not. 
- Numbers cannot be stored as any type other then `double` in `KahluaTable` which degrades performance and increases memory use.


### Java modding

This way of modding is not officially supported and is generally frowned upon by the community. However it offers many advantages over the official way which is why this guide promotes it as the **recommended** way of modding.

Still there are many examples where it makes more sense to use Lua over Java, such as when modifying user interface elements. Keep in mind that your mod can mix both Lua and Java depending on the need. The golden rule here is that any mod implementation that is either impossible to implement in Lua or can be implemented easily in Java should be written in Java, the rest should be written in Lua.

#### Advantages

- Nearly unlimited scope of modding.
- Type safety and access to all IDE features.
- Easy to inspect and debug your code during runtime. 
- Complete control over memory management.

#### Disadvantages

- More difficult to learn and use.
- Does not have officially supported API.
- Not supported by *most* of the modding community.

#### Recompiling

The old way of modding with Java is by modifying and recompiling game Java classes. 

Here are the steps that need to be repeated for each Java class:

- Decompile the game class.
- Build the class from decompiled sources.
- Check if new and old class have matching bytecode.
- If the bytecode does not match, modify the new class to match bytecode.
- Apply custom modifications to new class and build it.

There are three problems with this approach. The first one being that the process outlined above requires extensive knowledge of bytecode and is quite tedious to repeat for each class. The second problem is that every time we update the game to a new version we have to check if the game classes we are replacing have changed and then either repeat the aforementioned process or replace them with our custom classes. The last and most important problem is that there is no safe to distribute our mods to the community. If we upload the recompiled classes anywhere online we are essentially distributing parts of Project Zomboid which is a proprietary product protected under law. 

This method of modding is **not recommended** since it is tedious and not useful to the community as a whole.

#### The Storm Project

[Zomboid Storm](https://github.com/pzstorm/storm) is the new and *sexy* way of modding Project Zomboid.

It is a fully integrated Java modding toolchain that allows mod developers to easily create functional Java mods using a custom API. It is similar to [Fabric](https://fabricmc.net/) and [Forge](https://files.minecraftforge.net/net/minecraftforge/forge/) which both provide modding capabilities for Minecraft. The project is open source and licensed under [GNU GPL v3](https://www.gnu.org/licenses/gpl-3.0.en.html) license. It is currently in alpha stage of development and releases are publicly available on [Github](https://github.com/pzstorm/storm/releases). Everyone is encourage to join the testing process by downloading and using the latest pre-release. More information about Storm, including installation instructions and testing procedures can be found in the project [`README`](https://github.com/pzstorm/storm/blob/master/README.md). 

## Community

- Visit the [PZ Modding](https://theindiestone.com/forums/index.php?/forum/45-pz-modding/) section of the Project Zomboid forum to discuss and learn about modding.
- Join the official Project Zomboid [Discord server](https://discord.gg/EjSqDd9x) and visit the `#modding` channel to discuss modding.
- Join the unofficial Project Zomboid [Discord server](https://discord.gg/vCeydWCbd9) to meet the author of this guide and discuss and learn about modding.

