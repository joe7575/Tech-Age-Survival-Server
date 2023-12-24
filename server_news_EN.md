# Server News

### 16.09.2023

The new TechAge Assembly Tool is used to remove and reposition
Techage blocks without these blocks losing their block number.

### 28.08.2023

Update: A miniminer can:
- use `/points <name>` to display a player's points
- use `/msg_mm <text>` to send a text message to all miniminers
- use `/death_pos <name>` to query the death position of a player
- use `/last_died` to display the name of the player who died last
- use `/tp <name>` to teleport to other players
- start a poll with `/vote_kick <name>` whether the specified player should be kicked
- start a poll with `/vote_ban <name>` whether the specified player should be banned until the next server start
- start a poll with `/vote_mute <name>` whether the specified player should be muted until he/she rejoins again

### 25.08.2023

- The mod farming has been updated
- Only miniminers can participate in the `/vote_kick`.
- The TA5 generator now also has a generator menu for
  Start/Stop

### 09.06.2023

TA3 Flip-flop block added (see ingame documentation)

### 08.06.2023

Techage has two new blocks, the TA3 Command Converter and
the TA4 gaze sensor (see ingame documentation)

### 17.05.2023

The TA4 energy storage charge detector is new. It is used to
switch consumers on and off depending on the state of the charge
of an energy storage system.

### 05.05.2023

/tp command for miniminer restricted again, so that you can only
teleport to new players (playing time < 8 hours) or to unprotected areas.

### 01.052023

Bottles, glasses and crockery are now also available for purchase
in the furniture shop at the spawn.

### 28.04.2023

Any player with more than 100 hours of play and more than 100K points
(from the top 100 list) automatically gets 'miniminer' rights.
A miniminer can:
- use `/points <name>` to display a player's points
- use `/msg_mm <text>` to send a text message to all miniminers
- use `/death_pos <name>` to query the death position of a player
- use `/last_died` to display the name of the player who died last
- use `/tp <name>` to teleport to other players
- start a poll with `/vote_kick <name>` whether the specified player
  should be kicked

### 10.04.2023

- "Teleport Mode" added to TA5 Fly Controller.
- Added corrugated iron block ("myblocks:corrugated_iron").
- Added mod "extra_doors".

### 28.02.2023

- For some TA5 blocks, the number of required experience points
  has been reduced so that they can be used more easily.

### 27.01.2023

- Beduino has been reworked. The programs may have to be adjusted.
  Functionality of I/O module, input module, broker and router have
  been improved.

### 05.01.2023

- There is a new terminal for Lua and Beduino controllers.
  See README for instructions: https://github.com/joe7575/termlib
- Minecart cart terminals now also get a techage number
  and support the commands 'state' and 'distance'.
  See README for instructions: https://github.com/joe7575/minecart
- TA4 Detector got a "Countdown Mode".
  (As requested by ff999 from Discord)
- The file list in the programmer of the Beduino controller has changed.
  Own programs must therefore be slightly adapted.

### 11.09.2022

- TA4 Doser recipe can be controlled via Lua/Beduino commands.
- Pusher, Hopper and Signs Bot support for TA4 reactor
  added to switch catalyst item
- Sign Bot has new commands: jump_low_batt, jump_check_item, fall_down

### 04.09.2022

- TA4 pump and TA4 pusher now support the "flow limiter" operating mode.
  For example, a furnace/reactor can be filled with exactly the required
  amount of items. This can be set via the open-end wrench menu or
  via Lua/Beduino commands.

### 06.08.2022

- I temporarily deactivated the mod 'doc' because out-of-memory
  errors kept occurring

### 06.06.2022

- The mod Beduino is now fully integrated into techage and can
   can be used as an alternative to the Lua controller.
   See: https://github.com/joe7575/beduino/wiki

### 31.12.2021

- Hyperloop Tank/Chest are now stand-alone blocks.
  The blocks TA4 Tank/Chest must therefore be re-crafted
  in TA5 Hyperloop Tank/Chest.

### 28.12.2021

- The gas for the collider has been changed from hydrogen to
  isobutane as this is more realistic. Isobutane can be made
  with the reactor. Existing systems are subject to grandfathering,
  so they do not have to be changed.

### 25.12.2021

- It towards TA5 (future / fiction). The collider and some
  TA5 blocks are already available.

### 06.11.2021

- In addition to the "TA4 4x Button", the "TA4 2x Button",
  "TA4 2x Signal Lamp" and "TA4 4x Signal Lamp" are added.

### 30.10.2021

- Instructions for the TA4 Sequencer and TA4 Move Controller are
  now also available via the "TA Construction Board"
- Hazmat Suit mod added
  
### 24.10.2021

- TA4 Sequencer and TA4 Move Controller added
  Instructions (German) so far only here:
  https://github.com/joe7575/techage/wiki/TA4-Move-Controller-und-Sequenzer
- The number of commands sent to techage blocks per minute
  is now limited to 1200 per player.
  With `/ta_limit` your own current value can be queried

### 17.089.2021

- Matrix-Screens and mod 'ts_vehicles' added.

### 28.08.2021

  There is a new mod 'aloz'.
  This makes aluminum more important.

### 22.08.2021

- The Signs Bot has 3 new signs for
  making soup and cutting down trees

### 17.07.2021

- Techage has been updated to v1.0. This can lead to malfunctions.
   Notes on this in the "TA Construction Board" (first chapter)

### May 18, 2021

- Fixed grinder (flour) bug
- Fixed optical bug with concentrator
- Updated the unified_inventory, 3d_armor and ts_skins mods
- Added red stone, basalt and bauxite to the saw (moreblocks).
- other minor bugs fixed

### May 13, 2021

- There are 2 new concentrator tubes. With that you can
  several tubes can be combined into one tube.
- The grinder has some recipes for making flour
  receive.
- Added wall breakthrough for TA4 cable.
- Signs Bot can now be used on Distributors and Autocrafter
  access.
- Stairway Mod recipes became “cheaper”.

### May 10, 2021

- The fuel cell block has been upgraded. This
  can now also be configured as a Cat. 1 generator,
  so that storage systems can also be loaded with it.

### May 9, 2021

- The behavior of the distributors has been changed,
  so that this ver ratio of the items in the filters
  also map correctly to the outputs in the long term.

### May 6, 2021

After the bots stopped everywhere with malfunctions,
I restored the bot.
- The bot now delivers again when mining leaves
  just leaves
- The cutting command for sheets has been expanded for this purpose.
  This means you can plant leaves and harvest seedlings
  (Probability 1:20)
- The bot can now also sow peas

### May 4, 2021

Sign Bot improvements:
- added print command (debug function)
- The relevant error message is now also displayed
  Command issued
- techage command improved (for multiple words)

### May 2, 2021

- The Signs Bot now also delivers when mining leaves
  occasionally seedlings (just like real players).
- Reactor/Doser bug fixed (items were lost)
- The minecarts have been given a pusher (see
  in-game instructions)
- The towercrane mod has been updated. The cranes have
  now lighting.
- Fixed scroll bug on construction board

### May 1, 2021

- The importance of oil should be increased. Therefore
   was changed:
   - The recipe for the TA4 oven heater has been changed.
     You now have to use the TA3 oven heater first,
     to get the materials for the TA4 oven heater.
   - Bitumen is now always required for highway blocks
- The use of Digtron should be restricted.
  Therefore, Digtron can now only be used underground
  be (y < -35)

### April 24, 2021

- The minecarts are new. Because I change some things in the code
  had to, the buffers have to be reconfigured and the
  Unfortunately, routes have to be re-recorded. The carts
  but work as before. Additionally there is
  Speed limit signs, as well as a
  Cart Terminal, which contains all carts with positions
  displays.

### March 13, 2021

- Sun and wind will be used in electricity generation from now on
  higher priority than coal or oil.
- The heat exchanger on the energy storage device switches on
  again when the heat quantity falls below 95%.
  So far it has been 90%.
- The mod moreblocks has been updated. If anywhere
  If 'unknown' blocks have appeared, let us know.
  I may then have to define 'aliases' again.

### March 8, 2021

- The ICTA Controller now also has an 'exchange'
  Command for the door controller II.
- There is now also a TA3 injector for the TA4 injector.
  Both can now not only fill boxes in a targeted manner,
  but also empty. That should happen to almost everyone now
  Boxes work, including those from the Signs Bot.
- The Signs Bot can now also make compost. For that
  But composting now takes longer.
- The bot should no longer pick up the garden soil
  “Trampling” crops.

### March 2, 2021

- There are a few new blocks in myblocks (pattern),
  with which walls can be wallpapered to create patterns
  or to be able to create lettering. Leave the blocks
  turn with the screwdriver, as well as with right-hand
  click recolor.

### February 26, 2021

- The techage:ta3_doorcontroller2 now has a command
  'exchange'. This means you can now use the Lua controller
  Blocks can also be set/removed or exchanged individually
  become. For example, extendable stairs and...
  simulate something similar.

### February 22, 2021

- For everyone who was wondering what the strange one is for
  Logic block should be good: There is now a new one :)
- The pusher and also the Sign Bot can now
  Collect honey from the beehives (xdecor and farming).
- There is a new glass mod with XXL panes for large,
  colorful windows.

### February 16, 2021

- There are new TA4 laser beam blocks for wireless
  Electricity transmission. Everything else can be found in the in-game documentation.

### February 15, 2021

- The Signs Bot command 'cutting' has been expanded, like this
  that not only flowers, but also blocks
  Tree can be harvested.

### February 9, 2021

- The TA4 water pump was replaced by a TA4 water inlet
  Block replaced. This means the pump can now be at the tank
  to be placed. This means there is no power and no FLB
  more needed on the water.

### February 6, 2021

- There is now a TA4 recycling machine, the Techage
  and Hyperloop blocks can be recycled

### January 17, 2021

- There will be new Hyperloop networks, among other things
  a player network. Anyone with their own train station
  This network wants to be connected
  to the moderators, or directly to Discord
  report.

### December 30, 2020

- There are fireworks now. But only for 2 days.
  The mod will then be deactivated again (until
  next New Year's Eve)

### December 18, 2020

- There is a new "Door Controller II", everything
  more information in the construction plan.

### December 15, 2020

- There is a large post office right at spawn.
  Every player has the opportunity to
  to have a mailbox set up for you.
  Many of the currently active players already have one
  Get a mailbox. If you don't have one yet,
  Simply contact the server staff.

### November 18, 2020

- As announced, I have the mod digtron as follows
  configured:
  - Cycle time: 4 s
  - Max. number of digtron blocks: 25
  
### November 17, 2020

- The marketplace is open again.
  Here everyone can have one or more sales boxes
  set up to sell things.
  But there are a few rules that must be adhered to
  and are also on posters there.
  You can get to the market square with the Hyperloop.
- Advance notice: The digtron will be in its
  Processing power reduced to better
  to fit TechAge and also less server lag
  to produce. Just that you already
  be forewarned...

#### November 2, 2020

- The 8x2000 crate has been revised and can
  Now you can also stack or use new tools
  Pick up tools (thanks to Thomas)
- The wind turbine can now only be used in one
  real sea biome can be set up
  (more information in the construction plan)

### November 1, 2020

- There are 2 new blocks:
    - TA2 generator to work with the steam engine too
      to be able to generate electricity.
    - TA3 electric motor to also power TA2 machines
      to be able to drive.
- TA4 tank and crate can now be configured so
  that all players have access to the content.

### October 11, 2020

- There is a new mod: Paraglider
  To start, jump off a mountain and then immediately
  Use the paraglider item (left click).
  It is controlled with the 4 control buttons WSAD.

### October 8, 2020

- The batteries can now also be charged
  from the Lua controller via the 'load' command
  be queried, but the battery must be used for this
  be repositioned once.

### October 5, 2020

- The mods 'cottages' and 'ts_furniture'
   are now active at 'homedecor'
   more blocks activated.

### October 3, 2020

- There is a high performance distributor,
  which supports 8 entries per filter
  and is therefore more suitable
  to fill the '8x2000 boxes'.

### August 14, 2020

- The Hopper now also supports
  digtron, default:furnace and protector:chest

### August 3, 2020

- The mod simple_skins is active.
  You can create your own using the /skin command
  Change appearance/texture
  (Tip: You can use the F7 key
  see "from the outside")

### July 3, 2020

- Cracking and hydrogenation recipes
  added for the reactor

### July 2, 2020

- Added valve for the yellow tubes
- Fixed bug with highway blocks
- Basalt glass textures in the Techage
  Added gate/door blocks

### June 23, 2020

- Techage now has its JetPack. Instructions here:
  http://joesworld.zapto.org/wiki/pmwiki.php?n=Main.JetPack
- The JetPack requires the 3d_armor mod
- Unfortunately the skin mod no longer works

### June 14, 2020

- You now have to give the techage carts a number
- Via the chat command “/mycart” and the number
  the status of the cart can be queried
- The Hyperloop can now also go up and down
  be built.

### June 1, 2020

- TA4 sliders and distributors only reach
  full performance, albeit TA4 tubes
  be used.
- Signs Bot now has commands
  To implement loops and functions
  (https://github.com/joe7575/signs_bot/blob/master/README.md)

### May 14, 2020

Techage now has its own carts:
  - A tanker truck for liquids
  - A crate cart for items
Both leave things like tanks and boxes
Fill/empty slide and pump.
In this context, the mod
Minecart improved so that the new ones
trolley can be used optimally.

### April 15, 2020

- Added TA4 injector
- added the digtron mod

### April 15, 2020

- Signs bot bug fix
- Door controller bug fix
- 2 wall breakthrough blocks for tubes
  added
- The TA4 pipe inlet / TA4 Pipe Inlet
  can do no more than break through the wall
  be used!!!
- Documentation updated

### April 14, 2020

- Displays revised
- Operating modes of TA3/TA4 slide and
  8x2000 box changed (see
  https://github.com/joe7575/techage/wiki
  Chapter TA3 and TA4 or construction plan)

### April 11, 2020

- Added Display XL
- the TA4 8x2000 boxes can now become one
  size box can be connected
  (see construction plan)
- the illumination of the LED street lamp
  was improved
- The LED plant lamp has been changed. The
  Flowers now grow less quickly.

### April 7, 2020

- Bug in 8x2000 box with non-stackable ones
  Fixed items
- Several bugs im doser fixed
- Fixed water pump bug
- another alternative recipe for the TA2 box

### April 5, 2020

- the TA4 stone crusher has been upgraded. The
  Hole size is now adjustable
- The blocked/standby times of the machines
  were reduced
- the no-power error has been fixed
- the TA2 box has an alternative recipe
- Bug fixed in Hyperloop (crash from yesterday)

### April 2, 2020

The following bugs have been fixed:
- Power display for the fuel cell
- Protection at the pump
- Drilling turn "blocked" error
- Server removal error
- ICTA controller status query
- Lua controller status query
- Door controller error (door is gone)
Added lamp holder in 5 colors

### March 31, 2020

- The filter function on the TA4 slider works
  now for the TA4 crate and the TA4 8x2000 crate.
- The quarries/stone crushers have been completely overhauled
  works (on references from Franko)
- The Oil Explorer has been reworked. One can
  now also looking for oil underground, drilling
  and extract oil.
- Due to the changes to the Oil Explorer you can now
  Oil can also be found again in places that
  previously searched in vain.

### March 27, 2020

- There is a TA4 LED plant lamp
  Plants and also flowers underground
  to be able to grow.
- There is also a modern TA4 LED street lamp.
  (see construction plan)

### March 22, 2020

- TA4 crate/chest changed
- TA4 slider/pusher changed
- The TA3 door/gate blocks have been changed.
  There is now an additional one for that
  Door Controller.
All changes are in the construction plan
described.

### March 19, 2020

The mod emote is here, with the following commands:
- /sit - sit down
- /sleep - sleep as if in a bed
- /lay - lay down, just like sleeping
- /freeze - character stops moving as if frozen while walking
- /point - raise hand out to signal a direction
- /wave - do a quick hand wave
- /stand - used to revert back from other emotes

### March 18, 2020

- Other TA4 machines and special ones
  Added TA4 tubes

### March 17, 2020

- Switch, Player Detector and more
  Blocks for the Lua controller are
  available

### March 14, 2020

- The Lua Controller is there, for all Lua
  Programmers and those who want to become programmers.
  https://github.com/joe7575/techage/blob/master/manuals/ta4_lua_controller_EN.md

### March 9, 2020

- There is now also one for the ICTA controller
  German instructions at:
  https://github.com/joe7575/techage/blob/master/manuals/ta4_icta_controller_DE.md

### March 6, 2020

- The Tiger is disabled for now. Your
  Please send your opinion via /email to JoSto
  send.
- The capacity of the tanks has been doubled.
- Added instructions on how to oil
  can be transported via minecarts.

### March 5, 2020

- Bugfix: The hopper works again
  with the Wood Barrel from the compost mod.

### 03/02/2020

- The TA4 pipe inlet (techage:ta4_pipe_inlet)
  can now also be used as a wall duct for the
  yellow pipes can be used.
- You can make red stones from red mud and sand
  burn and process further.
- The ICTA controller has been improved. With it
  you can now control the power output/consumption of
  Read generators and batteries.
  There was also an error in the controller menu.

### March 1, 2020

- The TA4 controller with display and
  Signal tower is there. Machines can do this
  controlled and monitored. Everything
  more in the help (construction plan)

### February 22, 2020

- The mod techage has been updated. Therefore can
  there are problems with many blocks and machines
  give. Information on how to use the machines
  You can find out how to get it working again in the
  Techage construction plan or here:
  http://joesworld.zapto.org/wiki/pmwiki.php?n=Main.TechageSoftwareUpdate

### January 11, 2020

- I'm switching from copper on Monday
  on fiberglass. Since I have to work, that will be the case
  Server will be gone for a few hours. After that should
  but there are no longer any problems with lags.

### January 4, 2020

- You can now get one of the Minecart buffer stops
  Enter station name (first hit the block,
  then right-click to open the menu). Both have
  Station has a name, the block shows the connection
  (if necessary, update the data with a right click).
- New players now always start over
  designed starter area at the Hyperloop
  Station 24. Thanks to everyone who helped build it.
  (the restriction of rights to the
  I removed the starter area again)

### November 21, 2019

- Fixed bug in oil pump
- "Notice of Death" now only occurs once per player
- The capa command for the heat pump now delivers
  the value in % (0..100)

### November 19, 2019

- The Hyperloop is here!!!
  There are no instructions yet, but 2 videos on YT:
  https://www.youtube.com/watch?v=wNeCGb9ABfE
  https://www.youtube.com/watch?v=vOcQkfY9_No&t=414s
- Fixed distillation tower bug with full tanks
- Bauxite is now available between -50 and -500 meters
- Attention: The old epoxy resin canisters could be used
  stack, the new ones no longer. So if you still
  If you have epoxy resin in a box, stay away from me
  Let me know and I can replace it for you

### November 18, 2019

There were once again extensive changes. More details
please refer to the help/construction plan:
- the industrial oven now also runs on electricity.
- Industrial furnace operation improved.
- The chemical reactor for processing bauxite
  and other substances is there. Now you can do that too
  Aluminum will be made (used for Hyperloop
  needed).
- A silo block for powder and granulate items
  was added.
- Added TA3 gravel washer.
- Changed some textures and recipes. New materials
  are: bauxite, gibbsite, red mud, aluminum,
  various powders, plastic granules, lye, etc.
- Bauxite has to be mined and can be found
  between -50 and -150 meters

### 11/11/2019

- Obsidian can now also be used with the industrial furnace
  getting produced
- The steel-block to steel-ingot recipe works again
- The bronze-block to bronze-ingot recipe works again
- The wind turbine gives an error message
  now also via a blue marking,
  what or where it doesn't fit.
- Menu for the electronics factory revised.

### November 10, 2019

- Recipe for the street blocks (motorway) changed

### November 9, 2019

- The distillation tower is here!
  Petroleum must now be converted into bitumen, heavy oil, naphtha,
  Petrol and gas are broken down.
- The small generator only runs on gasoline,
  the industrial furnace only uses heavy oil, naphtha or
  Petrol. The power plant's oil burner burns
  everything, including oil.
- Further processing of the raw materials
  coming soon...

### November 8, 2019

- Behavior of the pump and tanks has been changed:
  - Pumps must now have a line with the tanks
    be connected. You can't do it right next to it.
  - Tanks no longer connect automatically
    with their neighboring tanks, but must be done individually
    be connected.
- The power terminal now also shows not charged
   Lamps on.

### November 4, 2019

- Fixed some bugs with "black blocks".
- Fixed pump bug. This occurred
  if two or more pumps were used.
- Added oil drum

### November 3, 2019

- Oil is now a liquid that is pumped through pipes
  and must be stored in tanks or barrels. In addition
  there is a tank and a pump. Serve as lines
  the yellow tubes.
- The existing oil items can be filled into a tank
  or, as before, burned in coal-fired power plants.
- The petroleum pump must now have a tank for the oil
  instead of being connected to a box.
- The coal-fired power plant can now be converted to oil.
  To do this, the firebox must be replaced with an oil burner
  become.
- The small generator and the industrial oven are already there
  converted to the oil system.
- All 3 can be refilled with oil using a pump.

### October 17, 2019

- Power terminal improved. So that this again
  If it works, it needs to be reconnected to a distribution box
  be set.

### October 11, 2019

- Phill's Pizza Mod is alternative
- Fixed bug in energy storage. If this one
  Doesn't work for you, just restart and if necessary.
  Pay attention to the error message (info text).

### October 6, 2019

- Electrolyzer and fuel cell are at the start
- Documentation on this has been updated
- further improvements regarding outgoing lamps

### October 5, 2019

- Solar inverter now consists of 2 blocks
  (both need to be reset).
- Improved the display of the electricity terminal.
- Fixed energy storage and inverter bugs.
- Output of the solar system reduced to 3 ku per element
  or 100 ku for the inverter.

### October 4, 2019

- Solar inverter now has an arrow for it
  Current direction. Display in the menu improved. On "Error"
  it now shows the cause as an information text.
- The Info Tool now also helps when searching for electricity
  cable breaks in which there are adjacent distributors
  and consumers marked with a cage. Just do it
  try. More about this in the manual.
- The energy storage now starts even if it doesn't otherwise
  Generator is connected to the grid.
- The inverter now checks whether there are no more
  Inverters are present in a solar system.

### September 30, 2019

The solar system is sharp. You can find the instructions for this
in the Construction Board under TA4 or on GitHub.

### September 29, 2019

The in-game manual (Construction Board) is now complete
in German and fairly complete. The texts are simultaneous
also available on GitHub so documentation.
https://github.com/joe7575/techage/blob/master/manuals/toc_DE.md
This change was quite complex and has taken me a long time
Pretty busy time. That's why there aren't any yet
other TA4 machines.

### September 14, 2019

You can get a list of all products via /offer
Have sales issued.
You can also search specifically for things using '/offer product'.
For 'product', just a few letters in the word
must occur.
In order for this to work, all menus in the shop boxes must be displayed once
be opened so that the items appear in the list.

### September 13, 2019

The heat storage system is now available. This replaces
the TA3 battery Box. The instructions in German have so far only been available on:
http://joesworld.zapto.org/wiki/pmwiki.php?n=Main.EnergieStorageSystem
The TA Power Pole Top for 4 directions now works
like a fence block, but can go in all 6 directions
Make connections.
The Autobahn mod works now. You are faster on the street
than the tiger, so can travel without danger.

### 09/05/2019

The Liquid Sampler is available as TA2 and TA3 Machine.
It has two tube connections, for empty buckets in and for
full buckets out.
The Robby can now grow hemp and also handle cactus.
The cactus must be dismantled at heights 1 and 2,
You have to leave the lowest level 0 so that the
Cactus can grow back.
So far the bot has not been able to “read” signs in unloaded areas.
This issue should also be resolved.
August 31, 2019
The TA4 wind turbine is here. A demo system is in the sea
between woofi and Gordini.
The following boundary conditions must be observed:
- can only be set up in the sea (min. 20 m distance from the shore)
- the Techage Pillar mast must be between 10 and 19 m high.
- at least 14 m distance to the nearest wind turbine
- Wind only blows from 5 a.m. to 9 a.m. and 5 p.m. to 9 p.m
- you first have to put the power cable up, then the cable
  "plaster" with the pillar blocks.

### August 29, 2019

There are 2 new logic blocks:
- The funnel from TechPack, which can also unload carts
- the Cart Detector, which recognizes a cart and it
  can also start again
This means that Mincart can now be automated using Techage alone
become. (https://vimeo.com/356753970)

### August 28, 2019

There are 3 new logic blocks:
- the Node Detector (similar to the Signs Bot Node Sensor)
- the Player Detector (similar to the TechPack Player Detector)
- the logic block that can be programmed
  multiple input signals to one output signal
  to be able to link.
  As always, there is short help for all 3 blocks.

### August 25, 2019

- Added Door Block and Gate Block. By both
  Blocks can change their appearance using the Block menu
  be set. Both blocks disappear,
  when they receive an "on" command and appear
  again with an “off” command.
- Power switch for normal house installation
  added (just looks different)
- The wrench now shows the temperature
  and the biome when you click on a block.
  If it is an “ocean”, it will too
  shows that a wind turbine can be created here
  (if there are any).

### August 24, 2019

- I renamed the logic blocks again, there
  I had made a mistake. The "unknown" blocks,
  If you already have one, you can use it
  Convert wrench.
- There is a signal lamp that you can use commands to control
  switch on/off. This lamp does not require electricity and
  can be colored with a spray gun.
- The sequencer and timer blocks are also back

### August 23, 2019

The following logic blocks have been added:
- TA3 Button/Switch to turn machines on/off
- TA3 repeater to forward on/off signals
- TA3 Detector for objects traveling through tubes,
  to recognize
- Techage Programmer to program the numbers more easily
Further blocks such as timers and sequencers follow

### August 22, 2019

There are a few smaller changes again:
- the TA3 terminal is now there. This allows you to change the status
  from machines (the terminal also has a help
  Command)
- The open-end wrench is now called
  Info Tool, because you can use it to get all kinds of information
  machines and blocks.
- The Power Terminal can now also be placed in front of a "plastered"
  Junction Box can be set.
- the missing recipes for "Sieved Basalt Gravel" will be added
  now displayed.
- The industrial oven now has an arrow
  Progress display as the silicon wafers last
  need until they are fully baked.
- The size of a power network is now 1000 nodes
  limited. The Power Terminal displays this value.

### August 20, 2019

- There are now solar cells for the street lamp. The
  Solar cell must be placed above the lamp,
  the electricity comes out from below. The solar cell stores
  the electricity for the night and switches the lamp on in the evening
  and off again in the morning. One cell can power 2 lamps.
- The Power Terminal (looks like a control cabinet)
  displays data from the power network if available
  an Electric Junction Box is placed.

### August 14, 2019

- Signs Bot now has 2 new signs for carts
  loading and unloading.
- There is now the Signs Bot Chest
- The normal carts can now be crafted again

### August 3, 2019

- There is now a cart dispenser again like on JM.
  This can be placed in any train station so that
  There is always a cart available. Carts can do that
  can no longer be crafted or collected.

### August 1, 2019

- The spawn has been enlarged. The protected area is now open
  north to the water.
- Minecart has 3 gravel blocks for a railway gravel bed
  These blocks are also protected by milestones.
- Techage has once again received an update about what you can do
  but can't see anything and hopefully nothing
  notices. But it was for the upcoming TA4 expansions
  necessary.

### July 28, 2019

- Sign Bot farming rules for rice, rye, barley and pepper
  changed so that this can be farmed with the Robby.
- The "Baked Clay Blocks" mod is now active.
- Added cart route plan item from maxx.

### July 20, 2019

- We hereby announce that from today the marketplace
  is opened near the spawn. Please provide the information first
  read at the market square and then build your shop.

### July 14, 2019

- Protector: There is now a Marketplace Block.
  The protected area of this block has 4 inner
  5x5 large zones for market stalls.
  These inner zones are not initially protected.
  Only when a player has a shop in one of these zones
  the zone is protected for that player.

### July 13, 2019

- Signs Bot: There is now an AND block.
  This can be connected to multiple sensors and
  only sends a signal when received from all sensors
  a signal was received.

### July 8, 2019

- Signs Bot: There is now a delay block,
  to be able to delay signals. This
  must be placed between sensor and actuator.
- In addition, the block sensor was changed so that
  you can set whether it has more or fewer blocks
  should react, or to both as before.

### July 7, 2019

- Power Station: "Water block" bug fixed in the boilers
- Sign Bot: Fixed bot recipe error
- Sign Bot: "no seed" error fixed
- Sign Bot: Dismantling error in the box fixed
- Techage: Power distribution changed again because of the lamp flickering

### July 6, 2019

- The "TA Power Line" (power cable) can now
  can also be laid diagonally, i.e. at an angle.
- In addition, the power cables are connected to the masts
  (TA Power Pole and Apple Wood Fence) now too
  protected by Minecart Landmarks.
- In-game help expanded.

### July 5, 2019

- Signs Bot: The robot now only works
  with Minecart carts, as the normal carts
  tend to lose items on the go.
- Signs Bot: The timer now stops when
  the area is not loaded. So time has to
  have passed “actively”. It may be that the
  Timer needs to be restarted (enter time),
  that it works again.
- Fixed power switch bug. Now 2 switches can
  can also be placed directly next to each other.
- No_power bug fixed. Machines that have electricity again
  are supplied, are now running again with normal
  Processing performance.
- Fixed power outage bugs.
- In-game help expanded and partly into German
  translated.

### July 4, 2019

- At felix7's repeated request, I have the shop mod
  and installed the money from Joe's mini world.
  However, money here can only be exchanged for gold, which we have
  So here is a gold-backed currency with a fixed rate.
  A “bank” shop is provisionally located at spawn. There
  You can exchange money or “buy” it with gold.
  Of course you can also exchange goods etc.

### June 2, 2019

- Help on techage has been further supplemented and partially
  already translated into German
- The techage help panel has been revised
- Fixed conflict in 'protector:chest' recipe

### June 30, 2019

- Fixed bug with TA1 Hammer and Mossy Cobble
- Tip of the day expanded
- With the screw wrenches you can now also use them
  Junction boxes are queried as to whether there is power.
  This should help troubleshoot wiring problems
  simplify.

### June 29, 2019

- “Tip of the Day” introduced.

#### June 28, 2019

- Menu of the Indian Furnace changed so that only items
  as a result will be displayed for which also all ingredients
  are in the Furnace inventory (Felix7 bug).
- Some TA3 blocks now have numbers and commands
  so that you can get status with them in the future
  can query. Try out which blocks report what,
  you can already do this with the end_wrench.
- Fixed autocrafter bug
- The values behind the states "stopped", "running" etc.
  I had to change again. Therefore, it may be that
  that not all machines will run the same again straight away
  they should. A power cycle should be done
  but always help.

### June 27, 2019

- The help for the Signs Bot in German is ready.
- Recipe for making Basalt from Basalt Cobble
  added.

### June 24, 2019

- Techage: The hopper has got marking, so you can
  can see the ejection side from above.
- The placement of the lamps no longer worked, this
  should now go again.

### June 23, 2019

- Signs Bot: The farming sign has been changed. Instead of "turn_off"
  the bot does a “turn_around” at the end.
- Signs Bot: There is a new command "low_batt" around the bot
  to be able to switch off before the power runs out.
- Techage: The oil drill was finished too quickly for me and was
  therefore slowed down to 1m/16s.
- Techage: The street lamp can now be hung up again
- The mod "doc" is now active, which is one of mods for help pages
  can be used. Minecart, for example, uses "doc" as help.
  The help can be started via the player inventory.

### June 22, 2019

- The Tiger no longer has players in a cart.
  You can therefore put the rails back on
  Laying floor.
- There are two new blocks for overland power lines.

### June 21, 2019

- There are new basalt disks available via the TA3 Ind.
  Furnace can be made. There are also
  thin slices and oversized slices.
- The recipe selection for the TA3 Ind. Furnace has been changed.
  When an item is placed in the Furnace's input inventory
  the selection of output items is reduced to
  Recipes in which the input item occurs.

### June 20, 2019

- There is now a small generator that has a max of 12 current
  can deliver.
- Coal Power Station: The "fuel" consumption when idling
  (no consumer active) was optimized from 10% to 2%.
- There is a new page in the techage help board
  to the oil burning times of the various generators.
- Lamps: The power supply to the lamps has been restored
  revised so that they no longer flicker.
- Signs Bot: Bug fixed so that the bot now leaves again
  and collect gravel.
- Signs Bot: The bot now needs electricity (8), is in 5 min
  loaded and can then be active for 6-10 minutes (each command
  costs one point, but dismantling costs 2 power points).
- The Stairway Mod from TechPack is active.
- The new news mod is active. 
- 