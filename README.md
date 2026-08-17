# 🌌 Universal Generator Basics 🌌
A guide to the basic uses and features of Universal Generator.

__Universal Generator__ is an AI Dungeon scenario that can be used to create prompts for custom scenarios, narratives, characters, and worlds. It can be found here:

${UG Scenario}

[__Glossary__](#Glossary)

__Contents__
- [Getting Started](#Getting-Started)
-

__Advanced Features__
- [Generate with Background Prompt](#Generate-with-Background-Prompt)
- [Play with Multiple Prompts](#Play-with-Multiple-Prompts)

### Getting Started

Before you start using Universal Generator, ensure your settings are properly configured. Improperly configured settings, particularly __Optimized Context__, are the number one cause of issues.

__⚙️Required Model Settings__

⚠️Optimized Context: ___MUST BE OFF___ (Gameplay -> Story Generator -> Memory System)

Context Length: 4000+  (Gameplay -> Story Generator -> Memory System)

Response Length: 200   (Gameplay -> Story Generator -> Model Settings)

Raw Model Output: On   (Gameplay -> Testing & Feedback)


Click __Generate__ then __Generate__ again.

<img src=https://github.com/FaraC-scripts/Universal-Generator-Basics/blob/main/Images/Generate.JPG />

You will be asked to enter a __Prompt Type__ and __Concept__.

__Prompt Type__ is the type of writing you want to produce. Typically, this will be a __genre__ (sci-fi, romance, etc.) plus a __writing type__. The generator has instructions for handling each of the following __standard types__:

__Scenario:__ An open-ended adventure that focuses more on exploration and freedom than producing a specific story.

__Narrative:__ An adventure tailored to specific characters and situations, intended to progress along a planned course.

__Short Story:__ An adventure with a limited scope, intended to last for just a few scenes.

__World:__ A prompt that builds out a world with factions, locations, lore, etc. Can be used as the __background prompt__ when using __Generate with Background Prompt__, or as the __background prompt__ when using __Play with Multiple Prompts__. World prompts typically don't include the __scenario__, __narrative__, __backstory__, or __style__ components, and so may not function well when used to produce an adventure on their own.

__Character:__ A prompt that creates a character from multiple components, going into great detail on a single individual. Character prompts are not meant to be used to create an adventure on their own. Character prompts can be used as a __protagonist prompt__ or __background prompt__ when selecting __Play with Multiple Prompts__.

<img src=https://github.com/FaraC-scripts/Universal-Generator-Basics/blob/main/Images/Prompt%20Type.JPG width=40% height=40% />

### Generate with Background Prompt

__Generate with Background Prompt__ lets you include a prior Universal Generator prompt when creating a new one. _The prompt created with this option will __not__ include components from the background prompt in its final output._

This option is useful, for instance, when creating a character to fit with a world or scenario when using __Play with Multiple Prompts__.


### Play with Multiple Prompts


### Glossary

__Generate:__ One of the two scenario options for Universal Generator. Generate creates a __prompt__.

__Play:__ One of the two scenario options for Universal Generator. Play uses a __prompt__ to run an adventure.

__Prompt:__ JSON-formatted text created from multiple __components__ that can be used with __Play__ or other Universal Generator-enabled scenarios to run an adventure. The final output of __Generate__ creates a __prompt__.

__Component:__ Modular parts of a larger __Prompt__. Each output from __Generate__ its own component, except the first, and each __component__ has its own topic. __Components__ have a title and multiple fields.

__Field:__ Information in __components__ is generated in Field: Entry format. The __field__ comes before the colon and describes the type of information contained in its __entry__.

__Entry:__ Information in __components__ is generated in Field: Entry format. The __entry__ comes after the colon and contains generated information about its __field__.
