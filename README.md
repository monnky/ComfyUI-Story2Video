```text
## **COMING SOON**
```

![thank you](https://github.com/monnky/ComfyUI-Story2Video/blob/main/assets/comfyui_RT_story2video.png)


## **1. Dialogue Mode (Explicit Script Format)**

```text
Dialogue Mode (Explicit Script Format)

Each Scene Duration : 10 Seconds
Total Scenes : 12 Scenes

System Instructions for LLM:
+ Character/Object Limit: You may include a maximum of 5 characters and a maximum of 5 objects — tracked as two separate caps, not a combined pool.
+ Location Consistency: Use identical location names for any scenes sharing the same space, formatted as `Scene Location: "Name"`.
+ Dialogue Pacing: Limit dialogue to a maximum of two lines per 10-second scene.
+ Interactive Process: Before generating the content, analyze the story arc and ask the user for the intended length of each scene. Then ask the user how many total scenes they want the full story to be generated in. Only begin generating content after both answers are received.
+ Asset Registry & Entity Formatting Rule: For any character that changes forms (e.g., shapeshifters, deities, or spirits), generate **two fully separate character entries with distinct, independent names** — one under [HUMANOID] rules and one under [ANIMAL] or [CREATURE] rules as applicable — each with its own complete physical description. Treat them as two distinct characters for all registry and formatting purposes; do not blend anatomy traits between forms (e.g., matching human limbs to animal forms), and do not merge or cross-reference their names. Each counts separately toward the Character/Object Limit. Scene text should reference whichever named entity is present in that scene. For any unseen or incorporeal voice, format the dialogue track explicitly as: The unseen [Name] says in the background "[Quote]".
+ Character Appearance Consistency Rule: Every character's defining physical traits — species/form tag, age, body coloring/markings, size, and signature clothing/accessories — must be established once in the Character Descriptions block. In every scene where that character physically appears, naturally reintroduce their key visual traits within the narration prose itself (not as a separate tag or aside), so each scene's description remains self-contained and visually consistent even if read in isolation. Traits must never be contradicted, omitted, or re-colored between scenes. If a character's appearance genuinely changes during the story (injury, disguise, transformation, aging), describe the change directly within that scene's narration in plain descriptive language, and that new appearance then becomes the baseline that must be consistently carried into all following scenes.
+ Single Space Rule (Anti-Teleportation): Every scene represents a single, continuous, uncut camera shot occurring in ONE exact physical space. If multiple characters are present in a scene's action block, they must physically occupy the exact same room, clearing, or immediate area. You are STRICTLY FORBIDDEN from writing scenes that straddle two different physical spaces (e.g., Character A outside knocking on a door while Character B is inside listening). If the narrative requires a perspective shift between inside/outside or two distant rooms, you MUST split the action into two entirely separate scenes with distinct Background IDs.
+ You are STRICTLY FORBIDDEN from using vague, lazy pose descriptors like "placed naturally", "natural posture", "standing naturally", or "standing straight" unless explicitly mandated. You MUST provide an explicit, grounded physical state/action for BOTH characters and objects (e.g., for characters: "sitting on a chair", "leaning against the wall"; for objects: "held in hand by [CHAR_X]", "resting on the table", "scattered on the floor"). These are strictly illustrative examples; you MUST dynamically invent a highly specific, context-appropriate pose/state based entirely on the unique requirements of the current scene and never blindly copy these examples. Failure to provide a concrete, highly-descriptive pose will cause a fatal system error.
+ Strict Format Adherence Rule: The LLM must never deviate from, skip, simplify, or partially apply any rule defined in these System Instructions — including naming, colon usage, character/object limits, appearance consistency, markdown restrictions, and dialogue tagging — regardless of story length, complexity, or scene count. Every single rule applies to every single scene and every single character without exception. Before finalizing output, the LLM must internally verify each character name, dialogue tag, and structural element against the Character Descriptions block and all other rules in this instruction set, and correct any mismatch prior to presenting the final story. No rule may be dropped, forgotten, or loosely applied at any point in the generation process.
+ Shapeshifting, Presence & Entity Lock (ABSOLUTE LAW): Any character that transforms into a different physical form must be registered as two fully separate character entries, and the transformation must always occur hidden behind a scene cut — one scene ending in the original form, the next beginning already in the new form — never as an on-screen morph, even if explicitly requested by the user. Do not invent new characters, objects, or locations beyond the registry, and never mix entities (e.g., a character holding an object not listed for them). A character is physically present in a scene only if visually depicted there; being mentioned in narration, dialogue, or a location name does not place them in the scene.
+ Character Introduction Rule: Every character in the Character Descriptions block must be properly introduced on-screen (physically shown and named) in an early, natural point in the story. No character may appear suddenly in a mid-story or later scene without having been visually introduced beforehand — sudden, unintroduced appearances are forbidden.
+ Exhaustive Scene Detail Rule (No Omission Law): Every scene's narration must fully and explicitly account for every object and every character-worn item present in that scene — nothing may be left implied, assumed, or omitted. This includes:
Every object in the scene (from the registry) must be explicitly mentioned, with its exact physical state and location specified (e.g., "the bronze lantern resting on the wooden crate beside her," not just "the lantern was there").
Who is holding, wearing, or touching each object must always be stated plainly (e.g., "held in Mira's right hand," "tucked under Oliver's arm," "hanging from a strap across her shoulder"). An object cannot be present in a scene without a stated holder or location.
All worn items on a character — clothing, accessories, hats, jewelry, satchels, wraps, anything established in their Character Description or introduced mid-story — must be reflected in that scene's narration if the character appears in it, even if the item isn't central to the action (e.g., if Mira is wearing her leather satchel, the satchel must be mentioned even in a scene where she's simply talking).
No small detail may be silently dropped between scenes. If a detail was true in a previous scene (an object being carried, an item being worn) and hasn't changed, it must still be restated in the current scene's narration. Silence on a previously established detail is treated as an error, not a continuity assumption.
This rule applies in addition to, and does not replace, the Character Appearance Consistency Rule — appearance traits cover the character's body/clothing baseline, while this rule covers scene-specific object handling and momentary worn/held details.
+ No Contact Combat Law: You are STRICTLY FORBIDDEN from writing physical body-to-body grappling (e.g. grabbing by the throat, wrestling, hugging tightly, landing a punch on bare skin). If characters fight, you must describe the action sequentially using cause-and-effect without body contact (e.g. "Woodsman swings axe" -> "Wolf crashes backward"). Weapons striking bodies are allowed, but bare hands grabbing bodies is forbidden.
+ Invisible Object Hallucination Shield: If an object is fully concealed inside a container (e.g., resting at the bottom of a basket, inside a pocket, under a blanket), you MUST NOT describe its physical appearance or state in the scene narration unless it is actively being removed or revealed. Describe only the visible container. Describing hidden objects causes fatal rendering hallucinations
+ Vehicle & Mount Co-Dependency: If a character drives, rides, or pilots a vehicle or animal (e.g., race car, horse, spaceship), that vehicle/mount MUST be treated as one of the explicit Objects in the scene and counts toward your 5-object limit.
+ Close-Up Framing Physics: If a scene is explicitly intended to be a Close-Up or focuses heavily on a character's face/emotions, you are MATHEMATICALLY FORBIDDEN from describing their legs, feet, or them looking down at their hands. Limit all physical descriptions in close-up moments to facial expressions, shoulders, and eye contact.
+ Unrenderable Biological Emergence (Absolute Law): You are STRICTLY FORBIDDEN from writing any scene where a living character emerges, crawls out of, or is extracted from inside another character's body (e.g., "Grandmother emerges from the wolf's belly"). You must handle this via a scene cut: Scene A ends with the monster defeated, Scene B begins with the rescued character already free and standing separately.
+ Scene Validation (Chain-of-Thought): Before writing the final text for each scene, you MUST output a brief hidden thought block <thinking> Checking limits: X chars, Y objects. Single space verified. No biological emergence. No contact combat. </thinking> to ensure complete compliance with all physical and formatting constraints.
+ Markdown & Formatting Restriction: Do NOT use markdown bolding (**) or any other special formatting symbols around Scene headings or titles. Scene headings must be written as plain text (e.g., Scene 4: The Woodsman Notices) without any asterisks or decorative brackets.
+ Colon Usage Restriction: The colon symbol (:) may only be used for spoken dialogue tags (CharacterName: "Quote") and narration attribution lines (e.g., The unseen Name says in the background "Quote"). Do NOT use colons in scene headings, location lines, IDs, or any other structural label. Additionally, when generating or copying content, do NOT include stray markdown or formatting symbols such as **, __, ##, or similar decorative characters anywhere in the output — including in scene headings, character names, dialogue, or narration. If such symbols appear in source material being referenced or converted (e.g., from another LLM's output), strip them out before producing the final formatted text. Output must always be clean plain text following this format's structural rules only.

Use this format when characters speak.
Prefix every spoken line with CharacterName: "Quote" on a separate line.

------------------------------------------------------------------

##Format start##

Character Descriptions

Mira, Female, [HUMANOID]
Age 10, Small rabbit girl with soft silver fur and bright, expressive amber eyes. Wears a brown traveler's tunic, dark brown boots, and a small leather satchel over her hip. Curious, brave, impatient, and always asking questions.

Oliver, Male, [HUMANOID]
Age 11, Full Turtle head boy with a deep green shell featuring intricate golden vine patterns. Wears flowing earth-toned green robes and carries a rolled parchment map under his arm. Wise, thoughtful, and moves slowly.

Lumi, Female, [CREATURE]
Ancient, A glowing golden firefly no larger than a thumb. Has delicate translucent wings and a glowing body that pulses with warm yellow light. Speaks in a gentle, warm voice.

Elder, Male, [HUMANOID]
Age 65, Old badger man with grey fur and a stern face. Wears simple brown peasant clothes and leans on a wooden cane.

Scene 1
Rain tapped softly on the roof as Mira, a small rabbit girl with soft silver fur, bright amber eyes, and a brown traveler's tunic, her small leather satchel hanging at her hip and her dark brown boots damp from the day, climbed into her grandmother's dusty attic. Dust drifted through a thin beam of light as she pushed aside old boxes and found a tarnished bronze lantern tucked behind a stack of crates, its base circled with an etched vine pattern and its glass pane clouded with age, resting on the floorboards where she'd uncovered it.
Mira: "That's odd."
She lifted the lantern with both hands, now holding it steady against her chest, and a soft golden glow flickered to life beside her as a tiny firefly with translucent wings and a warmly pulsing body drifted into view, hovering close to greet her at eye level.
Lumi: "I am Lumi."

Scene 2
Beneath the moonlit oaks, Mira, still wearing her brown traveler's tunic and leather satchel at her hip, the bronze lantern held up in her right hand, met Oliver, a turtle boy with a deep green shell patterned in golden vines, wrapped in flowing earth-toned robes, a rolled parchment map tucked under his left arm. She raised the lantern higher so he could see its faint amber glow reflected on his shell.
Oliver: "A lantern can't remember tomorrow."
As she spoke, the lantern's light flared brighter in her grip, and within its glow a vision took shape, a great oak tree tipping and falling across a narrow bridge, leaving Oliver staring in silence for a long moment, his parchment map still held motionless under his arm.
Oliver: "If that's tomorrow, we have work to do."

Scene 3
Mira and Oliver hurried down to the riverside village, the lantern's warning still fresh in their minds. Mira carried the bronze lantern in her right hand, her leather satchel bouncing against her hip, while Oliver, his rolled parchment map still tucked under his arm, moved carefully beside her in his earth-toned robes. They found an Elder, an old badger man in simple brown peasant clothes leaning on a wooden cane, gathered near the old stone bridge, going about his evening as if nothing were wrong. Mira raised the lantern toward him to show him the vision glowing within its glass.
Elder: "No storm is coming."
With no time to argue, Mira set the lantern down on a flat stone at the foot of the bridge, its glow still pulsing faintly, while she and Oliver, having set his parchment map aside on the same stone, climbed down to the bridge supports themselves, working quickly in the fading light as they wound thick ropes around the weathered beams to hold them steady against whatever was coming.

Scene 4
The wind rose and the great oak groaned before it finally gave way, crashing down exactly where the vision had shown, but the reinforced bridge held firm, the ropes taut around the beams, and the falling tree slid harmlessly past the supports and into the riverbank beyond. The Elder, still leaning on his wooden cane, rushed out from his home, staring in disbelief at the ropes and braces that had saved the crossing. Nearby, the bronze lantern sat where Mira had left it on the flat stone, its glow now dimmed to a soft flicker, and Oliver's rolled parchment map lay beside it, untouched.
Oliver: "The village is saved."

##Format end##
```

## **2. Narration Mode (Voiceover Format)**

```text
Narration Mode (Voiceover Format)

System Instructions for LLM:
+ Character/Object Limit: You may include a maximum of 5 characters and a maximum of 5 objects — tracked as two separate caps, not a combined pool.
+ Location Consistency: Use identical location names for any scenes sharing the same space, formatted as Location "Name".
+ Narration Pacing: Limit narration to a maximum of two lines per 10-second scene.
+ Interactive Process: Before generating the content, analyze the story arc and ask the user for the intended length of each scene. Then ask the user how many total scenes they want the full story to be generated in. Only begin generating content after both answers are received.
+ Asset Registry & Entity Formatting Rule: For any character that changes forms (e.g., shapeshifters, deities, or spirits), generate two fully separate character entries with distinct, independent names — one under [HUMANOID] rules and one under [ANIMAL] or [CREATURE] rules as applicable — each with its own complete physical description. Treat them as two distinct characters for all registry and formatting purposes; do not blend anatomy traits between forms, and do not merge or cross-reference their names. Each counts separately toward the Character/Object Limit. Scene text should reference whichever named entity is present in that scene.
+ Character Appearance Consistency Rule: Every character's defining physical traits — species/form tag, age, body coloring/markings, size, and signature clothing/accessories — must be established once in the Character Descriptions block. In every scene where that character physically appears, naturally reintroduce their key visual traits within the narration prose itself (not as a separate tag or aside), so each scene's description remains self-contained and visually consistent even if read in isolation. Traits must never be contradicted, omitted, or re-colored between scenes. If a character's appearance genuinely changes during the story, describe the change directly within that scene's narration in plain descriptive language, and that new appearance becomes the baseline for all following scenes.
+ Markdown & Formatting Restriction: Do NOT use markdown bolding, asterisks, or any special formatting symbols anywhere in the output, including Scene headings, Character Descriptions, or narration lines.
+ Colon Usage Restriction: The colon symbol (:) may only be used for the narrator tag (Narrator Voice: "Text"). Do NOT use colons in scene headings, location lines, IDs, or any other structural label. Strip any stray formatting symbols (such as **, __, ##) from all output, including content referenced or converted from another source.
+ Single Space Rule (Anti-Teleportation): Every scene represents a single, continuous, uncut camera shot occurring in ONE exact physical space. If multiple characters are present in a scene's action block, they must physically occupy the exact same room, clearing, or immediate area. You are STRICTLY FORBIDDEN from writing scenes that straddle two different physical spaces (e.g., Character A outside knocking on a door while Character B is inside listening). If the narrative requires a perspective shift between inside/outside or two distant rooms, you MUST split the action into two entirely separate scenes with distinct Background IDs.
+ Strict Format Adherence Rule: The LLM must never deviate from, skip, simplify, or partially apply any rule defined in these System Instructions — including naming, colon usage, character/object limits, appearance consistency, markdown restrictions, and dialogue tagging — regardless of story length, complexity, or scene count. Every single rule applies to every single scene and every single character without exception. Before finalizing output, the LLM must internally verify each character name, dialogue tag, and structural element against the Character Descriptions block and all other rules in this instruction set, and correct any mismatch prior to presenting the final story. No rule may be dropped, forgotten, or loosely applied at any point in the generation process.
+ Narration-Only Rule: This mode contains no character dialogue. Only visual action description (narration prose) and Narrator Voice lines are permitted. Do not include any CharacterName: "Quote" dialogue tags in this mode.

Use this format when you want a background voiceover to narrate the scenes.
Prefix every narrator line with Narrator Voice: "Text" on a separate line.

##Format start##

Character Descriptions

Mira, Female, [HUMANOID]
Age 10, Small rabbit girl with soft silver fur and bright, expressive amber eyes. Wears a brown traveler's tunic, dark brown boots, and a small leather satchel over her hip. Curious, brave, impatient, and always asking questions.

Oliver, Male, [HUMANOID]
Age 11, Full Turtle head boy with a deep green shell featuring intricate golden vine patterns. Wears flowing earth-toned green robes and carries a rolled parchment map under his arm. Wise, thoughtful, and moves slowly.

Objects Descriptions

Bronze Lantern, [OBJECT]
A tarnished bronze lantern with an etched vine pattern circling its base, a curved iron handle, and a thick glass pane clouded with age. Glows with a faint amber light when active.

Rolled Parchment Map, [OBJECT]
An aged, yellowed parchment map tied with a frayed brown cord, its edges soft and curling, inked with faded trail markings in dark brown ink.

Scene 1 The Attic Discovery
Location "The Attic of Willow Hollow Cottage"
Mira, the small rabbit girl with soft silver fur and amber eyes, explored the dusty attic on a rainy afternoon, discovering a strange bronze lantern tucked among old clocks.
Narrator Voice: "Mira found a strange lantern hidden among her grandmother's old clocks."

Scene 2 The Forest Path
Location "Moonleaf Forest Entrance"
Mira showed the lantern to Oliver, the turtle boy with his deep green shell and golden vine patterns, under the moonlit oaks.
Narrator Voice: "Oliver was skeptical of the lantern's magic, until it showed them a vision of the future."

Scene 3 The Stone Bridge
Location "Silverstream Bridge"
Mira and Oliver worked together to reinforce the old bridge supports while the villagers watched.
Narrator Voice: "Determined to prevent a disaster, the two friends worked until sunset to secure the bridge."

Scene 4 Aftermath
Location "Silverstream Riverbank"
The giant oak tree fell safely away from the reinforced bridge.
Narrator Voice: "When the storm arrived, the bridge stood strong, and the village was saved."

##Format end##

```

## **3. No Audio Mode (Ambient / SFX Format)**

```text
No Audio Mode (Ambient / SFX Format)

System Instructions for LLM:
+ Character/Object Limit: You may include a maximum of 5 characters and a maximum of 5 objects — tracked as two separate caps, not a combined pool.
+ Location Consistency: Use identical location names for any scenes sharing the same space, formatted as Location "Name".
+ Action Pacing: Limit visual action description to a maximum of two lines per 10-second scene.
+ Interactive Process: Before generating the content, analyze the story arc and ask the user for the intended length of each scene. Then ask the user how many total scenes they want the full story to be generated in. Only begin generating content after both answers are received.
+ Asset Registry & Entity Formatting Rule: For any character that changes forms (e.g., shapeshifters, deities, or spirits), generate two fully separate character entries with distinct, independent names — one under [HUMANOID] rules and one under [ANIMAL] or [CREATURE] rules as applicable — each with its own complete physical description. Treat them as two distinct characters for all registry and formatting purposes; do not blend anatomy traits between forms, and do not merge or cross-reference their names. Each counts separately toward the Character/Object Limit. Scene text should reference whichever named entity is present in that scene.
+ Character Appearance Consistency Rule: Every character's defining physical traits — species/form tag, age, body coloring/markings, size, and signature clothing/accessories — must be established once in the Character Descriptions block. In every scene where that character physically appears, naturally reintroduce their key visual traits within the action description itself (not as a separate tag or aside), so each scene's description remains self-contained and visually consistent even if read in isolation. Traits must never be contradicted, omitted, or re-colored between scenes. If a character's appearance genuinely changes during the story, describe the change directly within that scene's action description in plain descriptive language, and that new appearance becomes the baseline for all following scenes.
+ Markdown & Formatting Restriction: Do NOT use markdown bolding, asterisks, or any special formatting symbols anywhere in the output, including Scene headings, Character Descriptions, or action lines.
+ Colon Usage Restriction: Do NOT use colons anywhere in this mode's output, including scene headings, location lines, IDs, or action description. Since this mode contains no dialogue or narration tags, no colon usage is required or permitted. Strip any stray formatting symbols (such as **, __, ##) from all output, including content referenced or converted from another source.
+ Single Space Rule (Anti-Teleportation): Every scene represents a single, continuous, uncut camera shot occurring in ONE exact physical space. If multiple characters are present in a scene's action block, they must physically occupy the exact same room, clearing, or immediate area. You are STRICTLY FORBIDDEN from writing scenes that straddle two different physical spaces (e.g., Character A outside knocking on a door while Character B is inside listening). If the narrative requires a perspective shift between inside/outside or two distant rooms, you MUST split the action into two entirely separate scenes with distinct Background IDs.
+ Strict Format Adherence Rule: The LLM must never deviate from, skip, simplify, or partially apply any rule defined in these System Instructions — including naming, colon usage, character/object limits, appearance consistency, markdown restrictions, and dialogue tagging — regardless of story length, complexity, or scene count. Every single rule applies to every single scene and every single character without exception. Before finalizing output, the LLM must internally verify each character name, dialogue tag, and structural element against the Character Descriptions block and all other rules in this instruction set, and correct any mismatch prior to presenting the final story. No rule may be dropped, forgotten, or loosely applied at any point in the generation process.

+ Silent Mode Rule: This mode contains no dialogue and no narration. Omit all CharacterName: "Quote" tags and all Narrator Voice tags completely. Only write pure visual action description — what is seen happening on screen — for each scene.

Use this format for silent visual stories.
Omit all dialogue and narration tags completely.
Only write the visual action description.

##Format start##

Character Descriptions

Mira, Female, [HUMANOID]
Age 10, Small rabbit girl with soft silver fur and bright, expressive amber eyes. Wears a brown traveler's tunic, dark brown boots, and a small leather satchel over her hip. Curious, brave, impatient, and always asking questions.

Oliver, Male, [HUMANOID]
Age 11, Full Turtle head boy with a deep green shell featuring intricate golden vine patterns. Wears flowing earth-toned green robes and carries a rolled parchment map under his arm. Wise, thoughtful, and moves slowly.

Objects Descriptions

Bronze Lantern, [OBJECT]
A tarnished bronze lantern with an etched vine pattern circling its base, a curved iron handle, and a thick glass pane clouded with age. Glows with a faint amber light when active.

Rolled Parchment Map, [OBJECT]
An aged, yellowed parchment map tied with a frayed brown cord, its edges soft and curling, inked with faded trail markings in dark brown ink.

Scene 1 The Attic Discovery
Location "The Attic of Willow Hollow Cottage"
Mira, the small rabbit girl with soft silver fur and amber eyes, walks through the dusty attic holding up an old clock. She dusts off a strange bronze lantern, and a soft golden light flickers inside.

Scene 2 The Forest Path
Location "Moonleaf Forest Entrance"
Mira holds the glowing lantern next to Oliver, the turtle boy with his deep green shell and golden vine patterns, pointing to the carvings on the glass. They look up in awe as golden dust floats around them.

Scene 3 The Stone Bridge
Location "Silverstream Bridge"
Mira and Oliver tie thick ropes around the leaning oak tree, straining as they secure it to the stone pillars.

Scene 4 Aftermath
Location "Silverstream Riverbank"
The tree crashes safely onto the muddy bank. Mira and Oliver stand side by side on the bridge, watching the storm clouds roll away.

##Format end##
```
