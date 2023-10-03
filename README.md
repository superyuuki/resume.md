# resume.md
every single project I have worked on over the span of high school + reflections on the projects

## Middle School - Freshman Year
- [MTTT2](https://github.com/auriium/MTTT2)
  - My first minecraft plugin (server sided mod) ever, and one that never made it onto the main game network
  - It was really bad but taught me object oriented programming in middle school
- [Gunfight Tactics](https://github.com/auriium/GFT.git)
  - This was the third gamemode ever made on my old Minecraft server, ElytraForce. It was effectively a miniature game played inside minecraft, but added guns, bombs, and a gameplay manager and state machine in order to replicate the videogame Rainbow Six Siege
  - I learned a lot about project layout and project management rewriting this in order to match the rest of my server's code standards
- [AUtils](https://github.com/auriium/AUtils)
  - The first of many Spigot frameworks that I wrote in order to ease the writing of final projects
  - Not a very good Spigot framework and consisted of a few utilities that others had made and I had polished, combined together into a maven repo
  - Started my history of writing frameworks (oh boy)
- [BungeeSuite](https://github.com/auriium/BungeeSuite)
  - A step up in complexity from Gunfight Tactics, this Minecraft plugin (server sided modification code) was designed to run on both the overseer (proxy) server as well as multiple game servers and provide automatic moderation and management tools
  - Contained a chat filter using markov chains (later switched to regex)
  - First time I ever used webhooks, external libraries to add Discord support so whenever someone connected to the server or said a bad word I could see it in discord
  - Contained a messaging system complete with logging that was all done over the proxy server
  - Contained a SQL storage system for messages and punishments
  - Used a redis pub-sub system to provide local server and proxy-wide messaging, which I was really proud of
  - Basic delta compression for "money" (game currency) transaction logging (woah i'm a fintech)
- [ElytraLevels](https://github.com/auriium/ElytraLevels)
  - I eventually branched the money storage system and currency out into a separate plugin for domain clarity
  - I learned a lot about concurrent (multithreaded) programming and how to get multiple independent agents (the servers) to concede communication to eachother
  - ElytraLevels also contained a service provider interface that all other ElytraForce games could use to track money after matches
  - Never got to implement this with Gunfight Tactics or Railgun Royale :(
- [Gears](https://github.com/auriium/Gears)
  - My first attempt at a configuration library that could use either Yaml or XML through abstraction of maven packages
  - It sucked and i never used it in prod
- [Branch](https://github.com/auriium/Branch)
  - my first very abstract framework library
  - was designed to make "commands" (like linux console commands OR minecraft console commands) and command parsing a lot easier
  - used a node-tree design that I would become a huge proponent of
  - a modern analogue would be something like [clap-rs](https://github.com/clap-rs/clap)
- [Beetle](https://github.com/auriium/Beetle)
  - A huge library and my second attempt at making a general purpose minecraft mod framework, this one contained a lot more utilities and also much more abstraction
- [OpenTutorial](https://github.com/auriium/OpenTutorial)
  - The first ever commissioned code i wrote! The commissioner was not happy that i took like 2 months to finish his order.
  - Code designed to 
