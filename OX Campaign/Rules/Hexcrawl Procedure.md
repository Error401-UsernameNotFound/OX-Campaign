```
Created by Carl Hartmeyer: May 30, 2025
Moved by Aaron Brey: June 12, 2025
Edited by Carl Hartmeyer: June 12, 2025 (v0.0.2)
Moved again by Aaron Brey: June 13, 2025
Edited by Carl Hartmeyer: Jun 24, 2025 (v0.0.3)
```
v0.0.3

KEY PRINCIPLES
- The hex key is locations, not encounters. (Specific keyed encounters often create context problems since we don't know what group of players will find them, and also need to be refreshed every single time they are encountered.)
	- The hexcrawl includes a procedural mechanism for generating new wandering encounters in the form of encounter checks. This helps make every expedition feel unique, even when it's in a well-traveled area.
- Players should be able to make new discoveries
- Players should be able to get lost or otherwise go somewhere they weren't intending to find
- Every hex is keyed
- Hexes themselves are not a player-interfaced structure. Players should not need to care about precisely which hex they are in.

Hexes do not always need to include an adventure site. Many hex keys can simply be landmarks or other points of interest.

This hexcrawl is designed for 6-mile hexes.

#### Basic Procedure
A day is divided into six *watches* of 4 hours each. Each character may take one [[#Watch Actions|Watch Action]] per watch.

It is recommended that two watches are spent traveling, two watches spent resting, and two watches spent engaged in other activities.
> **Forced March:** If a character spends more than two watches traveling per day, they must make a Constitution saving throw at the end of each travel watch beyond the second (DC 10 + 4 per watch of additional travel). On a failure, they suffer two levels of exhaustion.

**Expedition Start**
- Obtain standing orders for watch actions and travel pace
- Determine their plan, etc.

**Each Watch** (Overview)
1. Determine watch actions (and travel pace, if applicable), typically based on standing orders
2. [[#Encounter Check]]
	1. Roll 1d12. On a 1, wandering encounter. On an 10+, exploration encounter if traveling.(Some travel paces, such as [[#Travel Pace|Exploration]], affect this probability.)
3. Resolve travel (if applicable):
	1. [[#Navigation by Compass Direction|Navigation Check]] (skip if following clear path)
		1. Navigator makes a hidden Wisdom (Survival) check against the hex's navigation DC. On a failure, they become lost. (If there is no navigator, the check automatically fails.)
			1. Players should not be able to immediately know if they've failed the check.
		2. If the players realize they are lost, interrupt the watch as they change their plans. Any actions after reorientation are part of the same watch.
	2. Mark hex progress & track movement according to travel pace
	3. Don't forget to describe!
4. Resolve [[#Encounters]] (may interrupt travel)
	1. Exploration encounter: keyed element of the hex
	2. Wandering encounter: based on regional encounter table
	3. May theoretically occur during any part of movement (although it's most convenient to resolve them at the end)
5. Resolve other watch actions (foraging, etc.)
6. Timekeeping (mark any known clock advancement, resource consumption, etc. for the watch)

> **How far can you see?**
> Using our 6-mile hexes, a PC that takes the trouble to get a good vantage point should be able to identify the terrain type of neighboring hexes. If they don't bother to do this, however, they probably aren't looking hard enough to tell.
> Mountains can be seen on the horizon from 72 miles (12 hexes) away, but it's difficult to tell exactly how far away they are.
#### Travel Pace

**Normal:** An expedition traveling at normal pace may not use Stealth checks to avoid detection.

**Slow:** The expedition is being purposefully careful. An expedition traveling at a slow pace:
- Gains advantage on navigation checks
- Can make Stealth checks to avoid detection
- Has its chance for a wandering encounter halved. (If a wandering encounter is generated, there is a 50% chance it doesn't actually happen.)

**Exploration:** The expedition is trying out side trails, examining objects of interest, and so forth. While exploring, an expedition:
- Can't use Stealth checks to avoid detection.
- Gains advantage on navigation checks.
- Has its chance for encounters doubled. (Roll for encounters twice per watch, instead of once.)

**Fast:** The expedition is moving hastily through the wilderness. An expedition traveling at a fast pace:
- Can't use Stealth checks to avoid detection.
- Suffers disadvantage on Wisdom (Perception) checks.
- Suffers a -5 penalty to navigation checks.

**TRAVEL SPEED TABLE**

| **Pace**    | **Per Hour** | **Per Watch**       | **Per Day**        |
| ----------- | ------------ | ------------------- | ------------------ |
| Fast        | 4.5 miles    | 18 miles (3 hexes)  | 36 miles (6 hexes) |
| Normal      | 3 miles      | 12 miles (2 hexes)  | 24 miles (4 hexes) |
| Slow        | 2 miles      | 9 miles (1.5 hexes) | 18 miles (3 hexes) |
| Exploration | 1.5 miles    | 6 miles (1 hex)     | 12 miles (2 hexes) |
> *Notes: 
>  - "Per day" on this table assumes travel for two watches (8 hours), i.e. a full day of travel without a forced march.
>  - A half-hex of travel distance is the distance from the center of a hex to its edge.*
#### Watch Actions
Watch actions are categorized into Travel, Active, or Rest. Tautologically, travel can only occur if all travelers are taking a Travel Watch action. Both Active and Rest watches are stationary.
##### Navigator
Travel Watch
The expedition’s navigator is responsible for making [[#Navigation by Compass Direction|navigation checks]]. A second navigator can assist, granting advantage to the navigation checks.

##### Pack-Puller
Travel Watch
A pack-puller is responsible for managing an expeditions pack animals. A pack-puller can lead a number of animals equal to their passive Wisdom (Animal Handling) score. (This number includes the pack-puller’s mount, if any.)

##### Sentinel
Active or Travel Watch
Only expedition members acting as sentinels during a watch may make Wisdom (Perception) checks to detect threats or notice anything out of the ordinary.

##### Tracker
Active or Travel Watch (see below)
**Finding Tracks:** Searching an area (hex) for tracks is an active watch action. The tracker makes a Wisdom (Investigation) check[^1] against the appropriate Track DC.
**Following Tracks:** Once tracks have been found, a tracker can follow the trail during a travel watch by making Wisdom (Survival) checks against the appropriate Track DC. A new check must be made each watch. If a trail is lost, it may be possible to reacquire it using the Finding Tracks action.

| Surface                                     | Track DC                   |
| ------------------------------------------- | -------------------------- |
| Very soft ground (e.g. snow, wet mud)       | 5                          |
| Soft ground (e.g. sand)                     | 10                         |
| Firm ground (e.g. fields, forest)           | 15                         |
| Hard ground (e.g. bare rock, stream-beds)   | 20                         |
| **Condition**                               | **Modifier**               |
| Multiple people                             | -2                         |
| Large group (6+ people)                     | -4                         |
| Very large group (20+ people)               | -8                         |
| Creature was bleeding                       | -4                         |
| Every day since the trail was made          | +1 per day                 |
| Every hour of rain since the trail was made | +1 per hour (+4 per watch) |
| Fresh snow cover since the trail was made   | +10                        |

##### Forager
Active or Travel Watch (see below)
Characters can forage during an active watch or while traveling at a slow pace. Foragers make a Wisdom (Survival) check against the Forage DC of the hex. On a success, the forager either gains 1 ration of food or finds a source of fresh water (allowing the expedition to drink their daily ration of water and for waterskins to be refilled). An additional ration of food or source of fresh water can be found for every 2 points by which the check result exceeds the DC.

##### Search
Active Watch
While a character is searching, exploration encounters may occur despite the fact that the party is not traveling. Searchers may also make Wisdom (Perception) checks and Intelligence (Investigation) checks to find hidden locations.
When an exploration encounter is rolled during a non-travel watch, only the Searching characters come across it directly.

##### Make Camp
Active Watch
During an active watch, a character can establish a camp suitable for four creatures if they have tents or similar equipment to shelter them. (Horses and similar creatures do not require tents, but must still be accounted for in camp preparations.)
If the expedition does not have equipment for shelter, the character can only establish a camp suitable for one creature (either themselves or someone else) per watch action.
Larger camps may be established by multiple characters working together or by working over the course of multiple watch actions.

##### Resting
Rest Watch
A character must take the Resting watch action for two watches in a row in order to gain the benefits of a Long Rest. (See the rules for Long Rests regarding which types of interruptions are possible without disrupting the Resting action.)
> **Lack of Sleep**
> If a character does not spend at least one full watch per day resting, they must make a Constitution saving throw (DC 16 - the number of hours they slept, if any). On a failure, they suffer a level of exhaustion.

##### Other Actions
Varies
If a PC takes an action that feels like it would take at least an hour or two of focused activity, that probably counts as a watch action.
If the PCs make a quick pit stop, such as to buy supplies in a village, that can be assumed to take at least one watch action. Longer stops effectively put the journey on hold until the PCs resume it.

#### Navigation
##### Navigation by Landmark
If the party is following a clear and unmistakable path, such as a road or river, they don't need to make navigation checks. The same is true if they are moving towards a visible landmark. (If they lose track of the landmark for more than a few minutes, they probably need to make a check.)

##### Navigation by Compass Direction
Navigators trying to move in a specific direction through the wilderness must make a navigation check using their Wisdom (Survival) skill once per watch to avoid becoming lost. They don't necessarily know whether they've failed the check -- the funny thing about being wrong is that it mostly feels like being right.

##### Becoming Lost
Characters who become lost may veer away from their intended direction of travel. Roll 1d10 on the diagram below:
![[veer_diagram.png]]
When lost characters exit a hex, they will exit through the face indicated by the die roll.

Lost navigators continue making a navigation check once per watch. If the check succeeds, they will recognize that they are no longer certain of their direction of travel. If they fail while already lost, their veer can increase but not decrease.
> **Example:** A lost party is already veering one hex face left when they fail another navigation check. A roll of 1-4 on the d10 would cause them to exit the next hex *two* hex faces to the left of their intended direction, but other results won't affect their veer at all.

Navigators who encounter a clear landmark or unexpectedly enter a new type of terrain can make an additional navigation check to realize that they've become lost.
> **Player Suspicions:** If the navigator thinks they might be lost, they should be permitted to make this check even if they aren't actually lost. A successful navigation check will truthfully reveal to them whether they are lost.

##### Reorienting
A navigator who realizes they've become lost has several options for reorienting themselves. Unless specified otherwise, none of these options are considered watch actions, and the players continue with the same watch once they have decided what to do.
> **Player-Driven Realization:** Some circumstances might cause the players to decide that they're obviously lost on their own. If they do, they should be permitted to take reorienting actions, even if they aren't actually lost.

First, the party can backtrack by following their own tracks using the [[#Tracker]] action. While successfully backtracking, the navigator may attempt a navigation check each watch to identify whether they were lost or not at that point. If they fail, they reach the wrong conclusion.
> Since the party is at the end of their own trail, they may immediately begin following their own tracks without spending a watch searching for them. (If they lose their old trail, however, they will still need to reacquire it again.)

Second, they can attempt to determine a compass direction with a DC 10 Wisdom (Survival) check. On a failure, randomly determine the direction the navigator thinks is correct.

Third, they can attempt to precisely determine the direction of travel to reach a known objective by making a navigation check using the hex's Navigation DC + 10. On a failure, they immediately become lost again.

If the party finds themselves at a known location, they automatically cease being lost (because they now know where they are). Of course, they still need to re-navigate to their destination.
Similarly, a party that identifies a known landmark ceases to be lost and may navigate according to the ordinary landmark rules. (There's nothing stopping them from misidentifying a landmark, however.)

##### Typical Navigation DCs

| Terrain         | Navigation DC |
| --------------- | ------------- |
| Desert          | 11            |
| Forest (sparse) | 12            |
| Forest (medium) | 14            |
| Forest (dense)  | 16            |
| Hills           | 12            |
| Jungle          | 15            |
| Moor            | 12            |
| Mountains       | 14            |
| Plains          | 10            |
| Swamp           | 13            |
| Tundra (frozen) | 11            |

#### Encounters
If the party is deliberately navigating to a location they've been to before, they are assumed to automatically encounter it once they enter the hex. Unfamiliar locations are encountered through either the [[#Encounter Check]] or a [[#Search]].

##### Encounter Check
Each watch, the GM rolls an encounter check (or two encounter checks if the party is traveling at an [[#Travel Pace|Exploration Pace]]). An encounter check is rolled on 1d12: a 1 indicates a wandering encounter, while a 10 or higher indicates an exploration encounter.

> **Encounter Location**
> When the PCs are moving, they're likely to have traveled through more than one hex. It's most convenient to assume the encounter occurred in the last hex of the watch, but you can also determine the encounter hex randomly or even select one yourself if you think it'll be interesting.

##### Exploration Encounters
Exploration encounters only occur during watches in which characters are traveling or otherwise exploring an area (such as through the [[#Search]] watch action). If the characters are resting or otherwise stationary, ignore all rolled exploration encounters.
An exploration encounter indicates that the party has encountered a major landmark within the hex. This will generally be the primary location keyed to the hex.
Some keyed features might be hidden and aren't necessarily identifiable as important landmarks at first sight. Typically, party members will need to make a Wisdom (Perception) or Intelligence (Investigation) check in order to identify a hidden feature.

##### Wandering Encounters
A wandering encounter can occur during any watch. They are typically creatures whose movement can bring them into contact with the expedition regardless of if the expedition is moving or not, but could be other similar phenomena (such as a drifting noxious vapor, or falling meteors).
Each hex has a wandering encounter table. This will typically be a link to the appropriate regional encounter table, but some hexes might have their own special encounter tables for especially localized possibilities.

[^1]: See PHB pg. 175, "Variant: Skills With Different Abilities"
