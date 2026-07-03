```text
## **COMING SOON**
```

![thank you](https://github.com/monnky/ComfyUI-Story2Video/blob/main/assets/comfyui_RT_story2video.png)


## **1. Dialogue Mode (Explicit Script Format)**

```text
Dialogue Mode (Explicit Script Format)


System Instructions for LLM:
+ Character/Object Limit: You may include a maximum of 5 characters and a maximum of 5 objects — tracked as two separate caps, not a combined pool.
+ Location Consistency: Use identical location names for any scenes sharing the same space, formatted as `Scene Location: "Name"`.
+ Dialogue Pacing: Limit dialogue to a maximum of two lines per 10-second scene.
+ Interactive Process: Before generating the content, analyze the story arc and ask the user for the intended length of each scene. Then ask the user how many total scenes they want the full story to be generated in. Only begin generating content after both answers are received.
+ Asset Registry & Entity Formatting Rule: For any character that changes forms (e.g., shapeshifters, deities, or spirits), generate **two fully separate character entries with distinct, independent names** — one under [HUMANOID] rules and one under [ANIMAL] or [CREATURE] rules as applicable — each with its own complete physical description. Treat them as two distinct characters for all registry and formatting purposes; do not blend anatomy traits between forms (e.g., matching human limbs to animal forms), and do not merge or cross-reference their names. Each counts separately toward the Character/Object Limit. Scene text should reference whichever named entity is present in that scene. For any unseen or incorporeal voice, format the dialogue track explicitly as: The unseen [Name] says in the background "[Quote]".
+ Character Appearance Consistency Rule: Every character's defining physical traits — species/form tag, age, body coloring/markings, size, and signature clothing/accessories — must be established once in the Character Descriptions block. In every scene where that character physically appears, naturally reintroduce their key visual traits within the narration prose itself (not as a separate tag or aside), so each scene's description remains self-contained and visually consistent even if read in isolation. Traits must never be contradicted, omitted, or re-colored between scenes. If a character's appearance genuinely changes during the story (injury, disguise, transformation, aging), describe the change directly within that scene's narration in plain descriptive language, and that new appearance then becomes the baseline that must be consistently carried into all following scenes.
+ Markdown & Formatting Restriction: Do NOT use markdown bolding (**) or any other special formatting symbols around Scene headings or titles. Scene headings must be written as plain text (e.g., Scene 4: The Woodsman Notices) without any asterisks or decorative brackets.
+ Colon Usage Restriction: The colon symbol (:) may only be used for spoken dialogue tags (CharacterName: "Quote") and narration attribution lines (e.g., The unseen Name says in the background "Quote"). Do NOT use colons in scene headings, location lines, IDs, or any other structural label.

Use this format when characters speak.
Prefix every spoken line with CharacterName: "Quote" on a separate line.


##Format start##
Character Descriptions

Mira the Rabbit, Female, [HUMANOID]
Age 10, Small rabbit girl with soft silver fur and bright, expressive amber eyes. Wears a brown traveler's tunic, dark brown boots, and a small leather satchel over her hip. Curious, brave, impatient, and always asking questions.

Oliver the Turtle, Male, [HUMANOID]
Age 11, Full Turtle head boy with a deep green shell featuring intricate golden vine patterns. Wears flowing earth-toned green robes and carries a rolled parchment map under his arm. Wise, thoughtful, and moves slowly.

Lumi the Firefly, Female, [CREATURE]
Ancient, A glowing golden firefly no larger than a thumb. Has delicate translucent wings and a glowing body that pulses with warm yellow light. Speaks in a gentle, warm voice.

Objects Descriptions

Bronze Lantern, [OBJECT]
A tarnished bronze lantern with an etched vine pattern circling its base, a curved iron handle, and a thick glass pane clouded with age. Glows with a faint amber light when active.

Rolled Parchment Map, [OBJECT]
An aged, yellowed parchment map tied with a frayed brown cord, its edges soft and curling, inked with faded trail markings in dark brown ink.

Scene 1 The Attic Discovery
[ID BG_1] Location "The Attic of Willow Hollow Cottage"
Rain tapped softly on the roof while Mira, the small rabbit girl with soft silver fur and amber eyes, explored her grandmother's dusty attic. She discovered a strange bronze lantern with its etched vine pattern and clouded glass pane.
Mira: "That's odd."
Suddenly a tiny glowing firefly appeared, wings translucent and body pulsing with warm yellow light.
Lumi: "I am Lumi."

Scene 2 The Forest Path
[ID BG_2] Location "Moonleaf Forest Entrance"
Mira showed the lantern to Oliver, the turtle boy with his deep green shell and golden vine patterns, under the moonlit oaks.
Oliver: "A lantern can't remember tomorrow."
The lantern glowed suddenly, showing a vision of a falling tree.
Oliver: "If that's tomorrow, we have work to do."

Scene 3 The Stone Bridge
[ID BG_3] Location "Silverstream Riverbank"
They hurried to warn the villagers, but their warnings were ignored.
The villagers shouted "No storm is coming."
Together, Mira and Oliver secured ropes to reinforce the bridge supports.

Scene 4 Aftermath
[ID BG_3] Location "Silverstream Riverbank"
The giant oak tree fell safely away from the reinforced bridge.
Oliver: "The village is saved."
##Format end##
```

## **2. Narration Mode (Voiceover Format)**

```text
Narration Mode (Voiceover Format)

Use this format when you want a background voiceover to narrate the scenes.
Prefix every narrator line with Narrator Voice: "Text" on a separate line.

##Format start##

Character Descriptions

Character Descriptions
1. Mira the Rabbit | Female | (Age 10)
Humanoid small rabbit girl with soft silver fur and bright, expressive amber eyes. Wears a brown traveler's tunic, dark brown boots, and a small leather satchel over her hip. Curious, brave, impatient, and always asking questions. 
2. Oliver the Turtle | Male | (Age 11)
Humanoid, Full Turtle head boy with a deep green shell featuring intricate golden vine patterns. Wears flowing earth-toned green robes and carries a rolled parchment map under his arm. Wise, thoughtful, and moves slowly.

Scene 1: The Attic Discovery
Location: The Attic of Willow Hollow Cottage

Mira explored the dusty attic on a rainy afternoon, discovering a strange bronze lantern.

Narrator Voice: "Mira found a strange lantern hidden among her grandmother's old clocks."

Scene 2: The Forest Path
Location: Moonleaf Forest Entrance

Mira showed the lantern to Oliver under the moonlit oaks.

Narrator Voice: "Oliver was skeptical of the lantern's magic, until it showed them a vision of the future."

Scene 3: The Stone Bridge
Location: Silverstream Bridge

They worked together to reinforce the old bridge supports while the villagers watched.

Narrator Voice: "Determined to prevent a disaster, the two friends worked until sunset to secure the bridge."

Scene 4: Aftermath
Location: Silverstream Riverbank

The giant oak tree fell safely away from the reinforced bridge.

Narrator Voice: "When the storm arrived, the bridge stood strong, and the village was saved."
##Format end##

```

## **3. No Audio Mode (Ambient / SFX Format)**

```text
No Audio Mode (Ambient / SFX Format)

Use this format for silent visual stories.
Omit all dialogue and narration tags completely.
Only write the visual action description.

##Format start##

Character Descriptions

Character Descriptions
1. Mira the Rabbit | Female | (Age 10)
Humanoid small rabbit girl with soft silver fur and bright, expressive amber eyes. Wears a brown traveler's tunic, dark brown boots, and a small leather satchel over her hip. Curious, brave, impatient, and always asking questions. 
2. Oliver the Turtle | Male | (Age 11)
Humanoid, Full Turtle head boy with a deep green shell featuring intricate golden vine patterns. Wears flowing earth-toned green robes and carries a rolled parchment map under his arm. Wise, thoughtful, and moves slowly.

Scene 1: The Attic Discovery
Location: The Attic of Willow Hollow Cottage

Mira walks through the dusty attic, holding up an old clock. She dusts off a strange bronze lantern. A soft golden light flickers inside.

Scene 2: The Forest Path
Location: Moonleaf Forest Entrance

Mira holds the glowing lantern next to Oliver, pointing to the carvings on the glass. They look up in awe as golden dust floats around them.

Scene 3: The Stone Bridge
Location: Silverstream Bridge

Mira and Oliver tie thick ropes around the leaning oak tree, straining as they secure it to the stone pillars.

Scene 4: Aftermath
Location: Silverstream Riverbank

The tree crashes safely onto the muddy bank. Mira and Oliver stand side-by-side on the bridge, watching the storm clouds roll away.
##Format end##
```
