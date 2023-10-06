# resume.md
every single project I have worked on over the span of high school + reflections on the projects

## Freshman Year
- [MTTT2](https://github.com/auriium/MTTT2)
  - My first minecraft plugin (server sided mod) ever, and one that never made it onto the main game network
  - It was really bad but taught me object oriented programming in middle school
- [**Gunfight Tactics**](https://github.com/auriium/GFT.git)
  - This was the third gamemode ever made on my old Minecraft server, ElytraForce. It was effectively a miniature game played inside minecraft, but added guns, bombs, and a gameplay manager and state machine in order to replicate the videogame Rainbow Six Siege
  - I learned a lot about project layout and project management rewriting this in order to match the rest of my server's code standards
- [AUtils](https://github.com/auriium/AUtils)
  - The first of many Spigot frameworks that I wrote in order to ease the writing of final projects
  - Not a very good Spigot framework and consisted of a few utilities that others had made and I had polished, combined together into a maven repo
  - Started my history of writing frameworks (oh boy)
- [**BungeeSuite**](https://github.com/auriium/BungeeSuite)
  - A step up in complexity from Gunfight Tactics, this Minecraft plugin (server sided modification code) was designed to run on both the overseer (proxy) server as well as multiple game servers and provide automatic moderation and management tools
  - Contained a chat filter using markov chains (later switched to regex)
  - First time I ever used webhooks, external libraries to add Discord support so whenever someone connected to the server or said a bad word I could see it in discord
  - Contained a messaging system complete with logging that was all done over the proxy server
  - Contained a SQL storage system for messages and punishments
  - Used a redis pub-sub system to provide local server and proxy-wide messaging, which I was really proud of
  - Basic delta compression for "money" (game currency) transaction logging (woah i'm a fintech)
- [**ElytraLevels**](https://github.com/auriium/ElytraLevels)
  - I eventually branched the money storage system and currency out into a separate plugin for domain clarity
  - I learned a lot about concurrent (multithreaded) programming and how to get multiple independent agents (the servers) to concede communication to eachother
  - ElytraLevels also contained a service provider interface that all other ElytraForce games could use to track money after matches
  - Never got to implement this with Gunfight Tactics or Railgun Royale :(
- [Gears](https://github.com/auriium/Gears)
  - My first attempt at a configuration library that could use either Yaml or XML through abstraction of maven packages
  - It sucked and i never used it in prod
- [**Branch**](https://github.com/auriium/Branch)
  - my first very abstract framework library
  - was designed to make "commands" (like linux console commands OR minecraft console commands) and command parsing a lot easier
  - used a node-tree design that I would become a huge proponent of
  - a modern analogue would be something like [clap-rs](https://github.com/clap-rs/clap)
  - [**Had a wiki!**](https://auriium.github.io/Branch/#/)
- [Beetle](https://github.com/auriium/Beetle)
  - A huge library and my second attempt at making a general purpose minecraft mod framework, this one contained a lot more utilities and also much more abstraction
- [OpenTutorial](https://github.com/auriium/OpenTutorial)
  - The first ever commissioned code i wrote! The commissioner was not happy that i took like 2 months to finish his order.
  - Code designed to be modular and run off a yaml based DSL allowing users to create tutorials of any kind with any amount of stages ('quests')
- [**Kommission**](https://github.com/auriium/Kommission/tree/master)
  - My third ever discord bot (BungeeSuite's Discord integration and a second so bad that i won't mention it here)
  - Designed to turn a discord server into an ad-hoc marketplace where people could sell arbitrary products and conduct safe transactions
  - The bot would escrow transactions made by the buyer over escrow, and transfer to the seller when the buyer marked the product as complete
  - Used *Kontainer* for data storage
  - Never got finished, and was impossible to build trust as a third party for
- [**Kontainer**](https://github.com/auriium/Kontainer)
  - My own replacement for [TestContainers](https://github.com/testcontainers). Initially I used TestContainers in my project because i needed to spin up an SQL server for JOOQ every time i wanted to compile DataLoader or some of my private projects, in order to do code generation based on schema loaded into the SQL server
  - Unfornately TestContainers was filled with bugs and when I went to go debug the issues I ran into the TestContainers codebase which was very messy
  - I got into an argument with one of the TestContainers maintainers on an issue (can't remember which) and afterwards was so annoyed that i ended up rewriting their whole library from scratch
  - It works okay :D which I think is good enough for a from-scratch solo replica of something maintained by many devs
- [OpenMinePlatform](https://github.com/auriium/OpenMinePlatform)
  - Another general Minecraft Modding library i built OpenTutorial off of. More specific than Beetle and designed to replace it. If i ever got back into minecraft i'd probably use this.
- [DataLoader](https://github.com/SolarMC-Dev/DataLoader)
  - One of the most overcomplicated and elegant systems i've ever had the (dis)pleasure of working on, a framework designed to store huge amounts of varied data and define minigame persistence logic.

## auriium -> superyuuki
when i joined SolarMC, my friend and mentor A248 had me switch to using 2FA because we wanted to enforce security best practices. Unfortunately the phone that I set up 2FA with had a fall and I can literally no longer log into the auriium account. now i use superyuuki and auriium interchangeably.

## Sophomore Year
**I joined BitBuckets FRC this year** and ** and so much of my time ended up going to either that or school :)
- [**FRC2022 Robot: Appa**](https://github.com/BitBucketsFRC4183/FRC2022-Rapid-React)
  - My first time working on a team in person! Solo wrote the logging layer and some unit tests, contributed code to every subsystem
  - Was the beginning of the framework known as Mattlib, at this time only Changeables and Loggables existed
- [**Synapse**](https://github.com/superyuuki/synapse-core)
  - Attracted by the idea of Free Money (TM) that twitch streamers made I decided to write my own Twitch Viewbotting application in order to capitalize on this using Go, a green-threaded language I had learned that I thought would be perfect for this application.
  - The engineering process came in two design interations: First, I decided to try an innovative approach and use AWS lambda to spin up a headless browser that would then use selenium to pretend to watch the videos (this did not work, but i learned AWS in the process)
  - I then wrote a go program to do the same thing but locally, and provide multiple methods of replicating twitch views. This never got finished as I realized at this point that it was probably illegal
- The various YuuKomponents
  - A variety of thought experiments on designing a YAML-based DSL that could be used widely, while still being easy to use in Java. Never got finished, but you can go through the many design iterations to see my thought process evolve
- [**YuuKonfig**](https://github.com/superyuuki/yuukonfig)
  - The culmination of 2 years writing frameworks and libraries, and probably my best library ever
  - Designed to turn java Interfaces into Yaml or Toml config files and handle serialization/deserialization effortlessly with no work from the user
  - Allows for not just nested configs, but nested *datastructures* and nested *ser/ de* unlike any other Java config library I've seen yet
  - Can hotswap toml or yaml and write serializers and deserializers independent of the language, super easy to add other config languages
  - Comparatively fast at runtime because all the interface-configs are manually implemented by ByteBuddy when configurations are loaded rather than when read, dynamic proxies aren't used in order to avoid invoke overhead
  - End user gets a really nice experience!!
- [**Shiv**](https://github.com/superyuuki/shiv)
  - Second best in my opinion of my libraries
  - Inspired by Dagger and Guice, I wanted to create a dependency injection framework for my FRC team that was simple enough for anyone to use
  - I've never seen a dependency injection framework (up to dagger) that didn't use reflection, annotations, or runtime analysis, so i came up with an ingenious (imo) system that would use a swappable service provider interface (SPI)
    - Instead of annotating constructors and letting runtime reflection find them, users would literally provide the constructors along with their dependencies, making use of the little used Java quirk where constructor functions behave as lambda functions using method references
    - At compile time the SPI would be fufilled with a Graph Analysis runtime which then could be used in tests to do all the analyses that normal DI frameworks have to do at runtime (checking recursion, finding dependency supply patterns, etc)
    - At runtime that SPI is fufilled with a lightweight hashmap storing the constructor lambdae, allowing the compile time tests to guaruntee that the code works and shaving off all reflection overhead
    - Contains a special DSL made entirely out of interfaces to replace annotation based DI
   
## Junior Year and Senior Year++
- [BitBuckets Wiki](https://github.com/BitBucketsFRC4183/bitbucketsfrc4183.github.io)
  - An automatically deploying wiki that takes markdown files in the git repository and deploys them using Github Actions to a Rustbook online
- [**FRC 2023 Robot: MCR**](https://github.com/BitBucketsFRC4183/bitbucketsfrc4183.github.io)
  - First in-person team lead by me!!
  - I introduced my framework, Mattlib, for the first time. It took the useful features from the year before like Loggables and brought them back alongside a unified setup system, providing abstractions over common motors and controllers
  - It was too complicated for the average part time Java coder, which cost us valuable development time during the season, and I also didn't teach it properly, costing us more confusion. Learned a valuable dev-ops lesson, and made Mattlib2 less confusing to use and less obstructive/overarching.
- [**BBLib** / Mattlib2](https://github.com/superyuuki/bblib)
  - Logging framework + Networking framework + configuration
  - some optimal control stuff
- [ARC Starsector](https://github.com/superyuuki/starsector-arc-mod)
  - Game mod for the videogame Starsector which adds in a unique faction complete with custom ships, weapons and FX.
