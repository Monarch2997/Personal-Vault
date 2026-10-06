## Looper
### Story:
You play as a Walmart clerk, you were working the gun stand when a strange man came up to you. He refused to show any ID and demanded a weapon. You reasonable declined him. He launched you into another realm.

Its just you and a gun in a seemingly endless series of odd passageways traveling through light and dark.  Your goal is to escape, all you have is your stand rifle and the bullets that came with it.  You do not know how many times you will have to use it. You will encounter different anomaly's in this realm. Some will be friendly, some not. Soon you learn of its name, Totem.

As you play, you discover that the stranger, who the realm calls 3rd Oracle, has less control over this realm than you first thought. You slowly wrestle control of the realm away from him, eventually fighting him in a mind battle and winning. You awaken back at Walmart, slumped over the counter, your rifle on the floor. The 3rd Oracle drops dead before you, and full control of Totem passes onto you, the 4th Oracle.

### Gameplay:
You wake up in strange hallways, enter a room, speak with a anomaly, learn story, and then either fight or move on. You have three stats you pick at the start, suave, weird, and power. Suave makes you better at being peaceful with anomalies, power makes you better at fighting, and weird makes you unlock hand motions faster


## Needed Systems:
### Score/Control:
Every encounter with an entity will increase or decrease your control, which is shown as a score. Once you reach a score of 100, you gain great control of the realm and can challenge the boss(stranger from the store). If you win the battle, your score goes to 10 million or some bs, you gain full control of the realm and win the game
### GameState 
Similar to unreal engines GameState that universally holds info between levels. You may be able to alternatively hold it in the player but its unlikely
### Freedom of Movement:
Only if that would not require destroying code from the movement section. If possible, the goal would be to move left and right.
### Tile-map:
This is to create a background, either to a travelable map or just to pass the player by
#### Walls
To control player movement down paths and maze options
### NPC Entity:
Another cube that has its own controller that seeks to interact with the player. They can be met, and then you can either talk your way out or fight your way out. Some weak minions must be fought.
#### Damage System:
This allows the player and the NPC to fight. I need HP, Damage per Attack, Enemy projectile, the ability to have on impact damage
#### Movement 
move on command and move natural
#### Dialogue:
When players first encounter an NPC, before they fight, they need to be able to speak with them first. Both entities pause, and a dialogue bar appears
### Save and Load
Figure out how unity creates saves and make sure to save player progress, ability scores, inventory, name, choices made, morality, and locations
### Portals:
Disable collision for player character, then begin to move them from point a to point b, then once arrived, enable collision
### Cinematic Screen:
Allow the game to change while pausing player input
### Player Character
#### Health and Armor
Player HP for handling combat
#### Inventory
holding all of the treasures, unique items, and weapons, preferably a list in a UI menu
Track ammo in inventory. Guns will not have reload for this game. Melee will not exist for player.
#### Ability Scores
Take a quiz during your "interview", this lets you determine physical stats. Go from 1-6, except for occult(0-2)
**Spend 9 points on either:**
normality: Effects how well you get along with entities
Titanic: Increase Health and damage
Shift: Increase speed and attack speed 
**Outside player selection:**
Occult: What tier of manipulations you have, player starts at zero

Describe yourself:
Ability to talk with customers = normality. 
General strength and physical capabilities = titanic
speed of work = shift

stats start at 1 and go up to 6
#### Morality
Take a quiz during your "interview", this lets you answer three questions of morality: System starts at 5. Lowest you can get is 1, highest in 9.
1. Are you a felon? [] Petty Theft(-1) [] Battery(-2) [] Falsely Accused(+2) [] No(+1)
2. If someone hungry stole a loaf of bread, how would you react? [] Allow it(+1) [] Look the other way(+0) [] Stop them(-1)
3. How would you handle an angry customer [] Fight them(-1) [] Leave(0) [] Calm them down(+1)
4. 1-3 is bad morality, 4-6 is decent morality, 7-9 is good morality
#### Name
Write name on interview paper
#### Weapons
One weapon slot which is set which the current weapon of your pick. Scan inventory list for items with the weapon tag. Then provide them as options for current weapon. If there was a weapon before, put it back in the list. Put the new weapon in the weapon slot and remove it from inventory list.
### Hand Tracker / Manipulation
#### Loop / Horns
Unlocks at Occult 1, right after first encounter. This lets you save the game. When acquired, create a save (right outside the first entity encounter). Going forward, Loop will create a save of your current state, then send you back to that previous save.
#### Rage or Resolve / Fist 
Unlocks at Occult 2, acquired in the mid-game. This lets you increase a stat during dialogue or combat, depends on your pick when Occult is raised to two. Rage increases your Titanic and shift slightly, while Resolve decently increases your normality.
# Prefabs:
## Player (improved)
## NPC
# UI
*Find a fitting font for the game*
## Character Creator
## Inventory + current weapon
## Pause Menu
## Manipulations
## Dialogue
## Combat?
# Design/Sprites
## Player
## NPC
## Tile-set
## Weapons & other inventory items
## Projectiles
