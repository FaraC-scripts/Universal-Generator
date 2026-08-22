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
- [Play](#Play)

__Advanced Topics__
- [Generator Settings](#Generator-Settings)
- [Modifying Component Templates](#Modifying-Component-Templates)
- [Creating New Component Templates](#Creating-New-Component-Templates)
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

Response Length: 200+   (Gameplay -> Story Generator -> Model Settings)

Raw Model Output: On   (Gameplay -> Testing & Feedback)


Click __Generate__ then __Generate__ again.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Generate.JPG />

You will be asked to enter a __prompt type__ and __concept__.

__Prompt type__ is the type of writing you want to produce. Typically, this will be a __genre__ (sci-fi, romance, etc.) plus a __writing type__. The generator has instructions for handling each of the following __standard types__:
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

___Before you continue___, make sure the __component sequence__ fits the type of prompt you want to create. You can enter _/list_ in Do or Say for a summary of what each component does or look at the __component templates__ in your story cards for full information on exactly what the generator will be asked to created.

## Creating Components

After your __initial output__ is generated along with its __component sequence__ you can create the components in that sequence by just pressing __continue__. The next component in your sequence is always shown at the bottom of each output.

If you would like to guide your next component, enter a __request__ into __Do__ or __Say__. ___DO NOT___ use __Guide__ in the Do/Say action bar. It will not work.

For instance, if your next component is Character, and you would like to create a pirate captain, you can enter _a pirate captain_ into __Do__ or __Say__.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Player%20Request.JPG height=80% width=80% />

If you would like to create a component other than the next component in your __component sequence__, you can enter the name of that component as a slash command.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Slash%20Command.JPG/>

__Note:__ You can still use slash commands to create additional components after your __component sequence__ has ended.

A list of components with basic descriptions for each can be seen by entering _/list_ in Do or Say.

You can also guide a component created with a slash command by including a __request__ after the command. For instance, if your next component is World, but you would like to create a pirate captain, enter _/character a pirate captain_ into Do or Say.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Slash%20Command%20with%20Request.JPG height=80% width=80% />

## Characters

Universal Generator characters can be contained in a single component, or creating using as many as a dozen, depending on the level of detail desired.

For a __simple character__, use the _/character_ command. It will look something like this:

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Character.JPG width=70% height=70% />

A __simple character__ contains a __name__ on the top line, before the hyphen, a __role__ (in parentheses after the word "Character"), as well as a __gender__, and relatively short __background__, __appearance__, and __personality__ fields. For most purposes, especially if the character isn't central to the story, this is enough.

However, sometimes you might want a more detailed character for your story. If so, you can create a __multi-component character__ by starting with a __character base__. 

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Character%20Base.JPG width=70% height=70% />

A __character base__ has a __name__, __role__, and __gender__ just like a normal __character__ component, but instead of __background__, __appearance__, and __personality__ fields, it has __age__, __from__, and __factions__ fields. A __character base__ is ___NOT___ meant to serve as a character on its own. Instead, it is the first component used in a __multi-component character__.

A character base should be followed by additional components in the __component sequence__ (or manually, using slash commands) that fill in the details of that character. For instance, if you used _character_ as your __prompt type__ and are making a protagonist for use in __Play with Multiple Prompts__, your __component sequence__ should start something like this:

> \## Component Sequence: Character Base, Background, Appearance, Personality

The resulting character prompt would consist of four components, the __character base__ as well as a full component detailing that character's __background__, __appearance__, and __personality__, providing considerably more depth to that character (and taking up a larger number of tokens in your context).

Whether you started with a __simple__ or __multi-component character__, you can add further information to that character with Character-type components (you can see them in __story cards__ under the _Component - Character_ category). Aside from those already mentioned, the components that work by building off of an existing __character__ or __character base__ component include: __speech__, __preferences__, __romantic preferences__, __relationship__, __attributes__, __class__, __abilities__, __clothing__, __equipment__, __inventory__, and __resources__. If you are building a character, choose the components that are most important. ___Using all of these at the same time is certainly not recommended.___

## Modifying Components

Components can be fully modified in the scenario text editor, however, certain rules need to be followed when modifying them. Here is a component broken into parts, with an explanation of how each can be modified.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Component%20Parts.jpg width=70% height=70% />

🟢 __Name:__ Some components, like __character__ and __location__, have names. Others, like __narrative__ and __style__, do not. If a component has a name, it will be on the first line and must be separated by the component type by a space, a hyphen, and another space " - ". __This part can be edited so long as the formatting is kept the same.__

🔴 __Component Type:__ The name of component being generated. __Do not edit this part.__

🟣 __Role:__ This is only present on the __character__ and __character base__ components, describing the narrative role of the character. It must be inside of parentheses, after the __component type__. __This part can be edited so long as the formatting is kept the same.__ However, keep in mind that the character you intend to play should have the __(Protagonist)__ role.

🟠 __Field:__ A field name which defines what the value that follows it describes. The bulk of each component are paired __fields__ and __values__. Each __Field: Value__ pair must be a single paragraph (must be on a single line). The field is what comes before the first colon, and each line __must have a field__. __This part can be edited so long as the formatting is kept the same.__

🟡 __Value:__ The text describing its __field__. __This part can be freely edited so long as it remains a single paragraph (a single line).__

## Final Formatted Prompt

When you reach the end of your __component sequence__, you will get the following message:

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Sequence%20Complete.JPG height=80% width=80% />

If you press __continue__ you will get a JSON-formatted __prompt__ that can be used directly in __Play__ or any __Toolbox__ scenario that accepts __Universal Generator prompts__.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Sample%20Prompt.JPG height=40% width=40% />

You can also get a final formatted __prompt__ by entering _/end_ into __Do__ or __Say__ at any point.

## Play

To use your __prompt__ to create an adventure, click on the final output's text box, click __edit__, select all and copy with __Ctrl-A, Ctrl-C__.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Click%20Edit.JPG height=40% width=40% />

Return to the Universal Generator base scenario and start a new instance. This time, you need to click __Play__, then __Play__ again.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Play.JPG height=80% width=80% />

Paste your __prompt__ when asked to do so.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Paste%20into%20Play.JPG height=55% width=55% />

# Advanced Topics

[Generator Settings](#Generator-Settings) - [Modifying Component Templates](#Modifying-Component-Templates) - [Creating New Component Templates](#Creating-New-Component-Templates) - [Generate with Background Prompt](#Generate-with-Background-Prompt) - [Play with Multiple Prompts](#Play-with-Multiple-Prompts) - [Prompt Cards vs Story Cards](#Prompt-Cards-vs-Story-Cards) - [Using Prompts in a Standard Scenario](#Using-Prompts-in-a-Standard-Scenario) - [Component Relationships](#Component-Relationships) - [Creating Placeholder Cards](#Creating-Placeholder-Cards)

## Generator Settings

Universal Generator has a number of settings that can be configured in the scenario. Settings are available in the Generator Settings story card (it should be the bottom-most card in Story Cards).

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Settings%20Card.JPG height=25% width=25% />

When you click on the card, there are configurable settings in the card's Entry.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Settings.JPG height=25% width=25% />

Settings can be changed by changing the values that come after the colon on each line in the Entry. ___DO NOT___ change the text before the colon.

Here are descriptions of what each setting does.

Components
- Set Maximum Component Size (_default: 150_): changes the maximum word count the generator is given for each output.
  - This should be about 75% of your __Response Length__, but can be adjusted up or down to preference.
  - If your __Response Length__ is 400, this should be set to 300.
- Set Field Size Multiplier (_default: 1.0_): a multiplier applied to the size values present in component template cards.
  - This greatly affects the average size of components, and if it is increased, __Maximum Component Size__ should be increased proportionally.
  - If this is set to 2.0, __Maximum Component Size__ should be 300.
- Default to Story Cards (_default: false_): If true, components are configured as __traditional story cards__. If false, components are configured as __prompt cards__.
  - __story cards__ are given triggers based on their name and appear at the back of context when triggered
  - __Prompt cards__ do not need to be triggered and always float in the middle of context
  - Individual cards can have their format swapped by including the _-s_ option in a component creation command, e.g., _/character -s a pirate captain_

Final Prompt
- Include Concept as Component (_default: false_): if true, the __concept__ you entered on starting the scenario will be included in the __final prompt__ as its own component.
- Include Relationships (_default: true_): if true, relationship connections will be added to the final prompt.
  - Relationship connections are small fields added to certain components that reference each-other, such as the __Relationship__ component and the connected __Characters__, __Location__ components and the __Regions__ they are within, etc.
  - E.g., if you have the _Eiffel Tower_ location and _Paris_ region, and _Eiffel Tower_ has _Paris_ as its _Within:_ field value,  the _Paris_ component will get _Locations: Eiffel Tower_ added to it in the final prompt.
- Enable External Use Formatting (_default: false_): if true, the final prompt will be formatted slightly differently to make it more compatible with non-Toolbox scenarios.
  - Enable this, for instance, if you are creating a character to paste into a placeholder or the __plot components__ of a standard scenario.
  - ___DO NOT___ enable this if you intend to use your prompt in __Play__, or in other Toolbox scenarios that accept Universal Generator prompts.

## Modifying Component Templates

The individual instructions given to the generator for each component are stored in your __story cards__. Each component has its own template card. These cards can be edited to better suit your needs.

Here is the __character__ template, broken down into parts, and how each part can be modified.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Template%20Parts.jpg height=30% width=30% />

🟢 __Name:__ If a template has a __name__ field. This field is used for scripting purposes. __DO NOT__ modify it.

🟢 **__ of:** Some components in the Character category have an **__ of** field rather than a name. This field is used to connect the components it produces with a __character__ or __character base__ card. This field is used for scripting purposes. __DO NOT__ modify it.

<img src=https://github.com/FaraC-scripts/Universal-Generator/blob/main/Images/Background%20of%20Field.JPG height=30% width=30% />

🟣 __Role:__ This field is only present on the __character__ and __character base__ templates. This field is used for scripting purposes. __DO NOT__ modify it.

🟠 __Field:__ A name for the information the generator will fill in on this line. __This part can be edited so long as it starts with _"> "_ and ends with a colon _":"_.__ If you want the AI to generate the name for the field, encapsulate an instruction in _"!{...}"_. E.g., _"> !{Ability Name}:"_

🟡 __Instructions:__ Instructions to the generator for how it should fill in this field. Instructions always start after the colon ending their associated __field__. __This part can be freely edited so long as it remains a single paragraph (a single line).__

🔵 __Size:__ A specialized instruction that creates a word count range the generator will try to keep this field within. Size always comes at the very end of the line, after the __instructions__, and must always be _"Size:"_ followed by a number. That number is about how many words this field should be. __For sizes, you can freely change the number listed. You can also add or remove the _"Size:"_ part from the end of any field.__

🔴 __Special Instructions:__ A special field that does not work in the same way as other fields. The generator will not be asked to fill this field in. Instead, the text here will be included in the generator's general instruction set for this component. __You can freely edit, add, or remove a _"> Special Instructions:"_ field. However, you can only have one such field per component.__ 

## Creating New Component Templates

The easiest way to create a new component template is to __duplicate and modify an old template story card__.

When creating a template, the following rules must be obeyed for the new story card:
- The card's __type__ must be set to __custom__, then in the text box that appears beneath the custom type, its type name must begin with _Component_. It can optionally include a subtype after a hyphen, e.g., _Component - Story_
- The card's __name__ must be component name, and the slash command used to create it. E.g., a new component named _Cuisine_ has the slash command _/cuisine_
- The card's __entry__ must be a list of __fields__, each on its own line. Each line must start with _"> "_, then the field name, then then a colon, then instructions for completing the field. See [Modifying Component Templates](#Modifying-Component-Templates) for a more detailed breakdown.
- The card's __notes__ must contain two pieces of information used by the generator. The first line must be a short description of what the component is, e.g., _A description of a region's food and cooking._ The second line must be the word Symbol, followed by a colon, then a single character, preferably a unique emoji, e.g., 🍴

## Generate with Background Prompt

__Generate with Background Prompt__ is a scenario option branching from Universal Generator's __Generate__ option. This option lets you include a prior Universal Generator prompt when creating a new one. _The final prompt generated through this option with this option will __not__ include components from the background prompt in its final output._

This option is useful, for instance, when creating a character to fit with a world or scenario when using __Play with Multiple Prompts__.

To use it, paste an existing formatted __prompt__ when asked to do so. This __prompt__ is the large text block starting and ending with square and curly brackets that __Generate__ outputs once its __component sequence__ is complete. 

## Play with Multiple Prompts

__Play with Multiple Prompts__ is a scenario option branching from Universal Generator's __Play__ option. This option lets you create an __adventure__ using up to three __prompts__: a __main prompt__ as well as an optional __protagonist prompt__ and __background prompt__.

__Main Prompt (Required):__ this is what you would normally paste into the basic __Play__ option. It typically contains the bulk of your components, including __narrative__ or __scenario__, __backstory__, __style__, and other critical components.

__Protagonist Prompt (Optional):__ this prompt should contain a __character__ or __character base__ component and other associated components, such as __clothing__. This prompt is treated to ___special processing___ in the following ways:
- Toolbox first looks for a __character__ or __character base__ component with the _Protagonist_ role, meaning a component with a top line like _Nadine - Character (Protagonist)_
- If Toolbox cannot find a protagonist, it sets the role of the first __character__ or __character base__ component it finds to _Protagonist_. If the first character is _Nadine - Character (Ace Pilot)_, it becomes _Nadine - Character (Protagonist)_
- Toolbox will then collect all Character-type components associated with the selected character (except __relationship__ components). These are the components that start with the character's name as a possessive on the top line, e.g., _Nadine's Clothing_. All other components in the protagonist prompt __will be discarded.__
- If the __main prompt__ has a character with the _Protagonist_ role already, __the existing protagonist component will be replaced__. If that old protagonist component was associated with any __appearance__, __personality__, or __speech__ components, those will __also be removed__.
- If the old protagonist was associated with any components that are also in the __protagonist prompt__, the old components __will be replaced__. E.g., if the old protagonist _Thomas_ had the _Thomas's Clothing_ component, it would be replaced by _Nadine's Clothing_.
- If the old protagonist was associated with any components that the new protagonist __does not have__, those components will be __kept and renamed to match the new protagonist__. E.g., if the old protagonist _Thomas_ had the _Thomas's Resources_ component, but the __protagonist prompt__ did __not__ contain _Nadine's Resources_, _Thomas's Resources_ will be renamed to _Nadine's Resources_.
- If the __main prompt__ had a named protagonist, all instances of that character's name in all components of the __main prompt__ will be replaced with the name of the __protagonist prompt's__ new protagonist e.g., all instances of _Thomas_ everywhere will be replaced with _Nadine_.

__Background Prompt (Optional):__ The components in the __background prompt__ can be anything, and might typically include __lore__, __location__, and supporting __character__ components. Anything that is low-priority information. It is also a good place to paste a prompt that creates additional __story cards__ (as opposed to standard __prompt cards__). All of the components from the __background prompt__ will be placed behind the __main prompt__ in context.

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
