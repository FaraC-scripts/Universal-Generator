# 🌌 Universal Generator Guide 🌌
A guide to the uses and features of Universal Generator.

__Universal Generator__ is an AI Dungeon scenario that can be used to create prompts for custom scenarios, narratives, characters, and worlds. It can be found here:

${UG Scenario}

[__Glossary__](#Glossary)

__Contents__
- [Getting Started](#Getting-Started)
- [Creating Components](#Creating-Components)
- [Characters](#Characters)
- [Modifying Components](#Modifying-Components)
- [Final Formatted Prompt](#Final-Formatted-Prompt)

__Advanced Topics__
- [Generator Settings](#Generator-Settings)
- [Modifying Component Templates](#Modifying-Component-Templates)
- [Generate with Background Prompt](#Generate-with-Background-Prompt)
- [Play with Multiple Prompts](#Play-with-Multiple-Prompts)
- [Prompt Cards vs Story Cards](#Prompt-Cards-vs-Story-Cards)
- [Using Prompts in a Standard Scenario](#Using-Prompts-in-a-Standard-Scenario)
- [Component Relationships](#Component-Relationships)
- [Creating Placeholder Cards](#Creating-Placeholder-Cards)

## Getting Started

Before you start using Universal Generator, ensure your settings are properly configured. Improperly configured settings, particularly __Optimized Context__, are the number one cause of issues.

__⚙️Required Model Settings__

⚠️Optimized Context: ___MUST BE OFF___ (Gameplay -> Story Generator -> Memory System)

Context Length: 4000+  (Gameplay -> Story Generator -> Memory System)

Response Length: 200   (Gameplay -> Story Generator -> Model Settings)

Raw Model Output: On   (Gameplay -> Testing & Feedback)


Click __Generate__ then __Generate__ again.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Generate.JPG />

You will be asked to enter a __Prompt Type__ and __Concept__.

__Prompt Type__ is the type of writing you want to produce. Typically, this will be a __genre__ (sci-fi, romance, etc.) plus a __writing type__. The generator has instructions for handling each of the following __standard types__:
- __Scenario:__ An open-ended adventure that focuses more on exploration and freedom than producing a specific story.
- __Narrative:__ An adventure tailored to specific characters and situations, intended to progress along a planned course.
- __Short Story:__ An adventure with a limited scope, intended to last for just a few scenes.
- __World:__ A prompt that builds out a world with factions, locations, lore, etc. Can be used as the __background prompt__ when using __Generate with Background Prompt__ or __Play with Multiple Prompts__. World prompts typically don't include the __scenario__, __narrative__, __backstory__, or __style__ components, and so may not function well when used to produce an adventure on their own.
- __Character:__ A prompt that creates a character from multiple components, going into great detail on a single individual. Character prompts are not meant to be used to create an adventure on their own. Character prompts can be used as a __protagonist prompt__ or __background prompt__ when selecting __Play with Multiple Prompts__. They are also the easiest to use in standard scenarios. For more information, see [__Using Prompts in a Standard Scenario__](#Using-Prompts-in-a-Standard-Scenario).

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Prompt%20Type.JPG width=60% height=60% />

__Concept__ is open-ended and optional. You can skip it, if you don't really know what you want to make. But giving the generator some guidance is always recommended, even if it's just a few words. However, you can also go into great detail in your concept. By default, the __concept__ is not directly included in the final prompt. However, this can be changed in the [__Generator Settings__](#Generator-Settings).

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Concept.JPG width=60% height=60% />

Once you enter your concept you will get an __initial output__, which the generator uses to guide component creation. Make sure these instructions fit the type of prompt you're looking to create.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Initial%20Output.JPG width=70% height=70% />

The __initial output__ is split into four sections: role, direction, component sequence, and rules. Of these four, role, direction, and rules are fairly straightforward: they give the generator textual guidance on how it should create components. They can be freely edited or even removed entirely.

The __component sequence__ does not guide the generator's writing, but it does control which components get created and in what order.

___Before you continue___, make sure the __component sequence__ fits the type of prompt you want to create. You can enter _/list_ in Do or Say for a summary of what each component does or look at the __component templates__ in your Story Cards for full information on exactly what the generator will be asked to created.

## Creating Components

After your __initial output__ is generated along with its __component sequence__ you can create the components in that sequence by just pressing __continue__. The next component in your sequence is always shown at the bottom of each output.

If you would like to guide your next component, enter a __request__ into __Do__ or __Say__. ___DO NOT___ use __Guide__ in the Do/Say action bar. It will not work.

For instance, if your next component is Character, and you would like to create a pirate captain, you can enter _a pirate captain_ into __Do__ or __Say__.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Player%20Request.JPG height=80% width=80% />

If you would like to create a component other than the next component in your __component sequence__, you can enter the name of that component as a slash command.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Slash%20Command.JPG/>

A list of components with basic descriptions for each can be seen by entering _/list_ in Do or Say.

You can also guide a component created with a slash command by including a __request__ after the command. For instance, if your next component is World, but you would like to create a pirate captain, enter _/character a pirate captain_ into Do or Say.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Slash%20Command%20with%20Request.JPG height=80% width=80% />

## Characters

## Modifying Components

Components can be fully modified in the scenario text editor, however, certain rules need to be followed when modifying them. Here is a component broken into parts, with an explanation of how each can be modified.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Component%20Parts.jpg width=70% height=70% />

🟢 __Name:__ Some components, like __character__ and __location__, have names. Others, like __narrative__ and __style__, do not. If a component has a name, it will be on the first line and must be separated by the component type by a space, a hyphen, and another space " - ". __This part can be edited so long as the formatting is kept the same.__

🔴 __Component Type:__ The name of component being generated. __Do not edit this part.__

🟣 __Role:__ This is only present on the __character__ and __character base__ components, describing the narrative role of the character. It must be inside of parentheses, after the __component type__. __This part can be edited so long as the formatting is kept the same.__ However, keep in mind that the character you intend to play should have the __(Protagonist)__ role.

🟠 __Field:__ A field name which defines what the value that follows it describes. The bulk of each component are paired __fields__ and __values__. Each __Field: Value__ pair must be a single paragraph (must be on a single line). The field is what comes before the first colon, and each line __must have a field__. __This part can be edited so long as the formatting is kept the same.__

🟡 __Value:__ The text describing its __field__. __This part can be freely edited so long as it remains a single paragraph (a single line).__

## Final Formatted Output

## Generator Settings

## Modifying Component Templates

## Generate with Background Prompt

__Generate with Background Prompt__ lets you include a prior Universal Generator prompt when creating a new one. _The prompt created with this option will __not__ include components from the background prompt in its final output._

This option is useful, for instance, when creating a character to fit with a world or scenario when using __Play with Multiple Prompts__.


## Play with Multiple Prompts

## Prompt Cards vs Story Cards

## Using Prompts in a Standard Scenario

## Component Relationships

## Creating Placeholder Cards

## Glossary

__Generate:__ One of the two scenario options for Universal Generator. Generate creates a __prompt__.

__Play:__ One of the two scenario options for Universal Generator. Play uses a __prompt__ to run an adventure.

__Prompt:__ JSON-formatted text created from multiple __components__ that can be used with __Play__ or other Universal Generator-enabled scenarios to run an adventure. The final output of __Generate__ creates a __prompt__.

__Component:__ Modular parts of a larger __Prompt__. Each output from __Generate__ its own component, except the first, and each __component__ has its own topic. __Components__ have a title and multiple fields.

__Field:__ Information in __components__ is generated in Field: Value format. The __field__ comes before the colon and describes the type of information contained in its __value__.

__Value:__ Information in __components__ is generated in Field: Value format. The __value__ comes after the colon and contains generated information about its __field__.
