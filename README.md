sooooooo, new gd version finally :3 - meaning all my mods have to b updated which is very fun

im not rly happy w/ a lot of the mods ive made so i think this is the perfect opportunity to fix that, heres wat i have planned - no guarantees abt when i get around to it

main thing is i want to make a big editor mod combining most of the editor mods ive already made, my plans for that are at the bottom soo

## Deprecated Mods
### Abandoned
#### might rewrite
- free select
- trigger context menus
- better easing select
- more select filters
#### prolly wont rewrite
- scroll inputs
- save parent
- confirm like
- percentage liked
- improved colors
- gamemode visualizer
- kill count

### Merged
- default object options
- quick fill
- scale input
- replace object
- better particles
- auto startpos
- text object utils
- free snap
- better select all
- better move menu (not updating on index but will b updated; might b merged)
- setup user coin
- trigger id search
- better object tab icons
- ruler

## Better Editor Trail
### Fixes
- push pr to index finally

## Trigger Indicators
### Features
- add animated arrows :3
- add trace mode (work like robtops impl)
### Fixes
- fix drag triggers
- fix the only necessary extras or wtv mode
- do wtv the fuck ery said
- update to geode v5 kms
- cleanup utils or smth

## Group Label Shenanigans
### Fixes
im too scared to touch the codebase, ill js update and pray it works

## \[big editor mod collection - like better edit but worse :3\]
mayb i should come up w/ a name-

i dont rly wanna *maintain* a million different mods anymore so ive settled on js making one big mod :3

mind u this'll prolly have way more stuff this is js wat i have come up w/ for now

### Settings
trigger indicators has already kinda proven using geode settings as very annoying and infeasible for something like this so the idea is
- a big paged menu kinda like this :3
```
   [some    [feature name]
   logo ]

<  [settings]    [settings]    [settings]  >
   [settings]    [settings]    [settings]
   [settings]    [settings]    [settings]
                ............          [⌕] // search expands and pushes dots aside or smth
```

### New
basically features i wanna impl *the silly way* (poorly) that may or may not alrdy exist

#### Template
- save a level as a "template" and all new levels will have wtv blocks were in that level + its level settings
- like the old better edit feature
#### Layer Input
- fuck you ive wanted to impl this for so long idc
#### Zoom Input
- self explanatory
#### Pivot Snapping
- but not like the mod that alrdy exists, it js snaps when let go instead of using keybind/button
#### Trigger UI Utils
- wip mod i made a while ago which changes some trigger ui
#### Exit Static Fix Button
- generates the extra static triggers needed for exit follow static wtv to work properly
- if 2.208 didnt alrdy impl that i havent checked :3c

### Merged
#### Default Object Options
- way more options (mayb steal from that other mod cuz idk how they did it without js a bunch of manual entries :3)
#### Quickfill
- fix the color bug if i haven't already
- add option to fill with next placed object as center (and also some kind of fallback if objects keep filling an area too large)
- mayb do wat creatorcreepy suggested and figure out an alg to optimize the area filled
#### Scale Input
- actually rewrite ts
- add back clipboard
#### Replace Object
- instead of edit menu icon - have a find and replace type bar in the top right with a button :3
#### Better Select All
- option to add a button somewhere in editor ui - not sure where yet
#### Setup User Coin
- reimpl popup to b more vanilla (like capelings mod)
#### Ruler
- oml use drawnode i was scaling ccsprites im actually kms </3
#### Auto Startpos, Text Object Utils, Free Snap, Trigger ID Search, Better Object Tab Icons
- js update version and cleanup a lil
