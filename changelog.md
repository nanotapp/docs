# Changelog

## In developement / Coming soon <a id="coming-soon"></a>

[Visit the issue tracker for more info](https://gitlab.com/warpkode/public/brewfather/boards).

## 1.7.5 - 21.04.2019

### New

* Updated local/offline database to a newer version, first load after update might take a few seconds longer than normal

### Fixed

* Dropdown scroll issue on iOS

## 1.7.4 - 15.04.2019

### Features

* Import \(and export\) hopstand/whirlpool temperature from \(to\) BeerXML if present

### Fixed

* Batch bug if SmartPID was enabled and you entered/exited the device modal

## 1.7.3 - 10.04.2019

### Features

* **New history function** in the data section of the settings page
  * Allows you to **watch** a changelog of certain changes of your batches
  * Allows you to **restore** deleted recipes or batches _\(Premium feature\)_
  * Allows you to **restore** a batch to a previous state _\(Premium feature\)_
* Show total fermentables amount and total hops amount in PDF
* Show water profile name, source and target in PDF
* Added new Bonsak malts
* Added new hops

### Fixed

* Sharing option on the new Safari version on Mac, now gives you the normal share dialogue with an option for native share
* Changing dry hop to another resets day/days option
* Fixed max ABV on Escarpment labs London yeast
* Fixed a rare issue where the batch could freeze on open
* Fix SmartPID heating/cooling icon when power = 0
* Deleting equipment profile not returning to list

## 1.7.2 - 26.03.2019

### New Integration

[**Plaato Airlock**](integrations/plaato/airlock.md) **is now integrated with Brewfather.**

### Features

* Fermentation chart
  * Now shows **Bubbles Per Minute** when using the new Plaato Airlock integration. Also shows **pH** and **Pressure** when recieved from [Custom Stream](integrations/custom-stream.md)
  * You can now **zoom** the **chart** by marking/seleting an area, or two finger gesture on touch device
* Added Warminster malts
* Summary: Negative diff numbers now have blue color
* Account page: now shows upcoming invoice and historic invoices

## 1.7.1 - 21.03.2019

### Features

* Shows % on fermentables in brew-sheet/read-mode and recipe share page and PDF
* Now shows all units for misc independent of unit settings
* Added Oat hulls and some other ingredients
* BJCP Style Guide: Specialty IPA 21B, Historical Beer 21B and Kellerbier 7C now selectable as its own base style for competition entry
* Added Brut IPA as a custom Specialty IPA BJCP style

### Fixed

* Fixed Set Temps from BrewPiLess when Fahrenheit
* Boil top-up water also inlcuded in sparge water amount by default in water calculator, to get correct total profile
* Fix fermentation chart temp scale

## 1.7.0 - 02.03.2019

### New Integration

SmartPID is now integrated with Brewfather for brew-day and fermentation control directly from Brewfather, [**more info here**](integrations/smartpid/).

### Features

* You can now edit your account name and profile image in the account page
* Manufacturing date field on yeast, integrated with yeast starter calculator
* Changed to a little thicker font on PDF
* Now shows time field on hop for first wort and mash hops when boil time is 0 \(raw beer\). To help with IBU calculations for raw beer

### Fixed

* Yeast calculator recalculating wrong amount when using gram as unit on the yeast
* Rice hulls \(adjunct\) no longer affect mash water calculation

## 1.6.3 - 22.02.2019

### New

* You can now add a tag when importing multiple recipes at once from BeerXML
* Amount of dry hop per volume shown below hops in recipe designer
* Improved PDF layout, changed font, line change now work in recipe notes, added recipe color box
* Fermentables with use **Bottling** will now use estimated bottling volume to determine gravity potential

### Fixed

* Fixed post-boil gravity not working properly since 1.6.2, fermentables added in fermenter now correctly uses fermenter volume to determine gravity again
* Fix kJ in alcohol tool

## 1.6.2 - 19.02.2019

### New

* When altering trub/chiller loss in the equipment profile, the brewhouse efficiency is reestimated instead of the mash efficiency
* When switching between Kettle and Fermenter as batch volume target in equipment profile, the profile will calculate new batch size so it matches fermenter volume on both settings
* Now only shows Mash efficiency when using Kettle as batch volume target, since it is the only efficiency needed to calculate correct OG for these types of eq. profiles
* Added a few new Norsk Malt grain

### Fixed

* Fix batch page freezing on brewing tab when on a extract recipe with 0 boil time and no hop stand \(no brewing stages or brewing steps for brew tracker\)
* Fixed various minor issues with using Kettle as batch volume target in equipment profile, you will now get same results from a recipe independent of batch volume target when they have the same values and volumes. If you have previously had success with using kettle as batch volume target you might need to tweak your profile a little
* Potential from sugar/extract now takes into account trub/chiller loss instead of using fermenter volume directly, this might slightly lower OG on recipes with trub/chiller loss were sugar or extract is used, depeding on the amount of loss in your equipment profile. This is a common error in _other tools_, and if you want your OG to match _other tools_, this _"feature"_ can be enabled again in the experimental settings.
* Fixed fermentable type was not set properly in recipe designer for _other_, _liquid extract_ and _adjunct_ after version 1.6.0

## 1.6.1 - 14.02.2019

### Fixed

* Now shows calculated boiloff in equipment profile when calc boil volume is enabled
* Fixed boiloff issue in batch summary when calc boil volume is disabled in equipment profile
* Fixed hopstand IBU issue that could occur sometimes
* Fixed rare issue that could cause the batch to load infinitely

## 1.6.0 - 12.02.2019

### Changed

First time you open the app there will now be a popup asking you to accept the terms and conditions. This will only show once, or if the terms are updated.

### Features

* You can now **add manual readings and get a fermentation chart** in your batch
* Added support for **stepped starters** and **improved the yeast starter tool** it will now show yeast cell count and pitch rate in recipe, and recalculate if the recipe changes. The data entered in the starter calculation tool within a recipe is remembered and stored in the recipe
* **New summary section in the batch**, this will recalculate the original recipe based on measured values and give you updated values and you can compare the original recipe values to the recalculated values. There is also the possiblity to view the adjusted recipe. You can also copy this recipe and/or its equipment profile. This way you can create an equipment profile from measured values.
* When deleting a batch it will now check if you have removed any ingredients from the inventory, and ask if you want to return it, also added undo remove from inventory button
* **Danish Beer Style Guidelines** \(DØLD 2017\)
* **New yeast** added WLP067, M29, all **Bootleg Biology yeasts**
* You can now **edit all fields on inventory ingredients** \(edit details button\)
* Support **IBU from fermentables** \(IBU per amount\), for hopped extract
* Updated Coopers Liquid Extract \(with IBU numbers\)
* Final gravity will adjust to not exceed max ABV defined on the yeast
* There is now a note in the account page if the application is running in offline mode / no contact with cloud database.
* You can now click directly on the different stages in the brew tracker to skip to that stage
* Added **Ramp Time in fermentation profile**, also visible in fermentation chart
* New equipment profile field **minimum HLT water amount**, define the minimum amount of suggested HLT water you want, so you can cover the coil or heating element
* New equipment profile field **minimum sparge water amount**, will take water from calculated mash water if possible to reach a miminum sparge water amount. Minimum mash water will be prioritized.
* **Brewie+** equipment profile with correct water amount calculation
* Show total sum of dryhops amount per volume in the hop summary

### Fixed

* Batch: Use Fermentation start date to count fermentation days rather than Brew Date
* Fermentation Chart: Fixed temperature y-axis when using Fahrenheit
* Fix hopstand temp on brew-tracker
* SG readings from remote logging devices are now rounded

## 1.5.0 - 15.01.2019

### Important

When logging with **Tilt**, **you must now attach it to the batch** rather than putting the batch name in the "beer name" field of the Tilt App / TiltPi. 

_Beer name will still work **temporarily** to not break any ongoing logging. If you have attached the Tilt, the attached batch will be prioritized over the "beer name" field._ 

_This is to simplify and avoid confusion where the batch is not logging even when attached because there is something entered in the beer name field._

### Changed

Power-ups \(integrations\) are now restricted to Premium users only. The free Premium period for new users are extended from 24 to 30 days to give some more time for new users to test these features. _Ongoing logging will not be interrupted._

### Features

* Added **Hop Summary** to recipe designer \(button next to add hops\)
* **Grain/Water ratio** and **Grain Absorption Rate** now has specified units, **L/kg** when using metric units, and **qt/lb** when using gallons and lbs
* When entering hopstand temperature directly on the hop addition, this temperature will now also be used to calculate extended IBU for boil hops, rather than the temperature from the equipment profile \(Only when **Calculate Aroma Hop Utilization** is enabled in the equipment profile, default on\). If multiple temperatures are present, it will use a weighted average. If you have not corrected for this manually before, IBU on your hopstand recipes might change to a more correct value
* Show **count** next to categories in Recipes and Batches page
* Show kJ in alcohol tool
* New export option for readings: CSV file
* You can now select overflow target for the sparge-water limit in the equipment profile. Now defaults to Top-Up Water \(Boil\) rather than Mash-Water
* When changing status the of a batch you will get asked if you want to update the date corresponding to your status change, if it is different from todays date
* Added fermentation start date field in fermentation tab of batch
* Last carbonation type used is remembered
* Inventory page: New toggle to show only items with negative inventory \(when negative inventory enabled\)
* Adjust \(add / substract\) button on the ingredients in the inventory
* _New section in settings for experimental features \(new features that is not yet completed or fully tested can be enabled in settings at your own risk - Premium users only\)_

### Fixed

* Fix OG scaling not working if Potential / Extract was missing on fermentable
* Show 0 as time on 0 min hops in PDF, rather than nothing
* Yeast starter volume will now always show as liters in the info box of the yeast starter calculator
* Fixed yeast starter calculator giving wrong volume when using Chis White \(No Stir\) formula and gallons as unit
* Custom water formulas in equipment profile will now always be in metric units
* Removed some duplicate Weyermann grains
* Set type "Grain" on fermentables if imported with an invalid value

## 1.4.0 - 21.12.2018

### Features

* Added the possibility to **export your user data** for local backup in one JSON file \(bottom of settings page\)
* Added new power-up called [Custom Stream](integrations/custom-stream.md), allows you to hook in any custom device for logging fermentation data, for more details, [see here](integrations/custom-stream.md).
* Added HLT water and Total Water on print/PDF
* Added new field "tempUnit" to BrewPiLess logging format, allowed values are **C** and **F**, it will then log the temperature based on the given unit

### Fixed

* Made brew-sheet/read-mode selectable in all pages where it is used
* First Wort hops now shows in brew tracker
* Trub/Chiller loss now included in calculation of beer color \(the **color of your recipes might be lowered slightly** to a more correct number\)
* Now shows a warning if custom water fomulas have syntax error, rather than failing
* Fixed undo/redo in recipe designer when editing from batch view
* Fixed pluss button on ingredients in recipe designer when editing from batch view

## 1.3.4 - 13.12.2018

### Features

* Added **Mecca Grade Estate Malts**
* Added option in the edit reading to update the last reading shown under the completion bar for the batch \(refresh icon next to the delete icon\)
* If you have entered a FG on the batch, the entered FG will be used for the completion bar, rather than the last reading

### Fixed

* Fixed an error where the recipes page could forget what categories where collapsed when loading the page on a slow device

## 1.3.3 - 11.12.2018

### Features

* Hydrometer calibration temp is now remembered/stored

### Fixed

* Pre-boil gravity could get higher than OG when using mashtun loss \(unrecoverable\)

## 1.3.2 - 05.12.2018

### Features

* Added HLT volume as additional text next to sparge water amount when HLT deadspace is present
* If you click on a brew-tracker in the menu the batch will open _\(note: you must have opened the batches page at least once since the app loaded for this to work\)_
* Increased the height of the taste note textbox a little

### Fixed

* Fixed rare issue where one or more settings could reset to the default value \(example the Tilt turning off\)
* Strike temp now shows even if there is ramp time on the first step in the mash profile
* HLT Deadspace in the equipment profile is now added to the water amount the brew tracker suggest to prepare in your HLT

## 1.3.1 - 19.11.2018

### Features

* Inventory checkbox \(planning tab of batch\) is now red when inventory amount is less than recipe amount and negative inventory is enabled
* Visual: Added color transition on beer icon of recipe

### Fixed

* Allow to set negative inventory \(when enabled\) from batch planning tab
* Hops total amount now updates when scaling recipe
* Fixed rare issue where recipe did not load when equipment was missing

## 1.3.0 - 15.11.2018

### Features

* Recipe designer: You can now undo and redo changes in the current session \(currently desktop mode only\)
* Pressured fermentation: Added pressure to fermentation profile steps
* Now shows age since bottling date when batch has completed status \(batches page\)
* Refractometer tool: Now remembers calibration factor
* Settings page: Added reset default data button. This will allow you to reset the pre-included ingredients and profiles. When you click it you will be prompted about what you want to reset, and you have to confirm it
* Profiles: Added a delete button on the profiles in addition to the hidden delete button when you slide them in the list
* Inventory: New setting in the settings to allow negative inventory \(disabled by default\). When this is enabled you are allowed to write negative amounts in the inventory, or when checking off ingredients in the inventory they will become negative if you remove more than you have. \(Usefull if you have the ingredients you need to brew, but need to order the dry-hops for example, or you just want to enter negative amounts for things you want to buy\)

### Fixed

* No longer detaches device when changing device settings \(offsets\)
* Fermentable type not set on BeerXML import
* Unable to turn off brew tracker in a special situation
* When using SG+Plato as gravity unit it no longer shows plato in style guide ranges due to space issues

## 1.2.3 - 03.11.2018

### Features

* _**Normal**_ **is now the default FG calculation method for new users, current users have to change this manually in the settings if desired**
* Recipe designer shows a bigger beer color icon in desktop mode
* New unit setting, you can now choose to show gravity in **SG,** **°Plato**, SG+**°**Plato or **°Oe**
* You can separately select what gravity unit you want to input, choose between **SG**, **°Plato** or **°Oe**
* Added full yeast range of Escarpment Yeast Laboratories
* Added Idaho Gem and Sabro hops
* Supports CO₂ extract hops

### Fixed

* Fixed issue where top-up water was suggested in a rare case when min mash water limit was not reached, and max sparge water limit was set
* Brew tracker handles better when using it on multiple devices simultaneously and one of the devices closes the app/sleeps
* Now shows fermentation chart even if the logging device is no longer found / deleted

## 1.2.2 - 29.10.2018

### Features

* Camurri Brauer CB50 + CB50 MAXI equipment profiles
* Brewtools B40pro profile
* Updated Brewtools B80pro profile

### Fixed

* Allow remote logging to batch in Conditioning status again
* Starter volume now shows correctly as liters in recipe designer when using gallons
* Fixed rounding issue at the inventory manager in planning tab of batch
* Fixed text wrapping at the inventory manager in planning tab of batch

## 1.2.1 - 23.10.2018

* Fixed minor issue where recipe sorting did not update when changed

## 1.2.0 - 23.10.2018

### Features

* New **Devices page** in the menu, here you can see all your logging devices and change settings or delete them
  * Page will only show if you have at least one device activated in the settings
  * The last log from your devices is shown in the Devices page
  * Configure flat gravity or temperature adjustment to your devices. For gravity adjustment enter the number of gravity points to adjust in whole number\(s\). The adjustments will be applied to new loggings, it will not change previous logs
* **New remote logging** integration with ****[**MyBrewbot**](integrations/mybrewbot.md)\*\*\*\*
* You can now **attach and detach Tilt** devices to the batch similar to the other devices, this is optional. "Beer name" in Tilt needs to be empty for this to work. You can still log using batch number as beer name.
* Mash/Sparge water calculation method dropdown in equipment profile \(select between Default, No Sparge, and Custom\)
* **Brewtools B80pro** equipment profile \(will be tuned based on user feedback when the device is available\)
* Added description field to equipment profile
* Added malt from **Bonsak Gårdsmalteri**
* Added some **Polish and French hops**
* You can now add **\[SG\]** to the name of your iSpindel if you use SG based formula, it will then be logged correctly
* Added support for **Relative Bitterness Ratio** in recipe designer, displayed below BU:GU ratio, click to enable style range
* Shared recipe page now live reloads if owner changes the recipe

### Fixed

* Volume of measured values on PDF now displayed in the selected unit
* Starter size is now always in liters
* Now supports comma in water formulas
* Remote logging to batch will now be blocked if batch is in status Conditioning or Archived, in addition to Completed

_Version number note: From this version the second number in the version will increase when new features are released. The last number will increase when only minor changes or bugfixes occur._

## 1.1.25 - 12.10.2018

### Features

* Added/updated fermentables

### Fixed

* iSpindel server URL showed full url rather than just the end \(occured in 1.1.24\)
* Improved load time of batches page when closing a batch
* Max color in style range showed 0 when undefined max range

## 1.1.24 - 11.10.2018

### Fixed

* Missing ID on urls provided for utility in the settings. If you are still missing and id in the url, turn the toggle off, then on again, which will generate an id for you
* Unable to save fermentation/mash profile when temp was 0 in a step

## 1.1.23 - 09.10.2018

### Features

* Added BJCP Provisional Styles 17A. **Burton Ale**, 21B. **New England IPA**, X4. **Catharina Sour**, X5. **New Zealand Pilsner**
* Added two new sub-**status**es for batches: '**Conditioning**' and '**Archived**'
  * These statuses does not have its own tab, but will show as its own status in the batches page
  * Conditioned days now shows when status is Conditioning \(based on bottling date\), to set conditioned status, the batch must be in fermenting status first
  * To set Archived status, the batch must be in completed status first
* **Statuses** can now be **collapsed** in bathes page
* When creating a new batch, it will now **automatically open the new batch**, if a batch is already open it will be saved and closed
* You can now **drag and drop tags** to reorder them
* Tags now have autocomplete in recipe designer
* Allow spaces in tags
* Style bar for color now shows SRM/EBC as text instead of "Color"
* Added **Copy** button on **inventory** items to copy them. Also slide items to left to copy them directly in the inventory view
* Added delete button on ingredients \(you can also slide them left in the list to delete\)
* Inventory: show user notes on ingredients, user note is now also searchable
* Improved some step intervals \(amount adjusted when using arrow up/down keys\) on temperatures, hop and acid
* **Hopcat / Brew Monk / Brewster Beacon 30L** equipment profile \(mash-tun deadspace and trub-loss might be different on Hopcat and Brew Monk, will add a separate profile for those in a later patch\)

### Fixed

* Brew tracker enabled itself when entering brew tab even after having turned it off \(only if not started\)

## 1.1.22 - 26.09.2018

### Features

* New visual representation of the style guide values in recipe designer
  * Toggle showing BU:GU as style indicator by clicking on BU:GU under the IBU in the Hops section
* Ingedients page now lists in stock ingredients, click to quickly edit them
* Now remembers the last **main** page the app was on \(per device\) and loads it when opening the app

### Fixed

* Fixed timezone issues with date pickers

## 1.1.21 - 16.09.2018

### New Premium Feature

* Show, **edit** and **delete** raw values from Tilt, iSpindel and BrewPiLess. Click the edit button on the readings. Edit and delete is restricted to Premium users only

### Features

* Batches page: 
  * List brew date on planned batches, and days until planned brew day
  * Show fermentation day on batches in fermentation
  * Show days after bottle day \(conditionig days\) on completed batches
* Show hop type and hop year on inventory listing in batch planning stage \(new batches only\)
* Added Denali hop

### Fixed

* Fixed editing/deleting of batch log notes, issue occured only if you deleted a note that was not the first note
* You can now select future years in batch brew date and batch bottling date date selectors

## 1.1.20 - 13.09.2018

### Beta Test Feature

* Added an additional option for FG estimation, called "Normal", selectable in the settings.  _This method uses fermentable **type**, not fermentablility **%** like the advanced option. When using this, yeast attenuation % should be set to the max value from the manufacturer._  _Give it a try and submit your feedback_

### Features

* Added additional amount field in the add fermentable window, allow input of oz when using lbs, or grams when using kg
* Updated info on some yeasts
* Sparge temp, ambient temp and grain temp now imported from BeerXML if available
* iOS only: enabled autocorrect for some textarea fields, other devices should have it already

### Fixed

* Extract only recipes: Preboil Gravity now includes sugar/extract \(Recipe type = Extract\). This will improve IBU calculation for extract only recipes
* Other recipes: Preboil gravity now inlcudes sugar/extract when use equals mash or use is boil and time equals boiltime
* When equipment batch volume target is Kettle: OG calculation improved for sugar/extract additions
* Fixed invalid date error when month is set to december in the batch note log
* Fixed BeerXML import did not always import the mash profile steps

## 1.1.19 - 29.08.2018

### Features

* Refractometer Tool: New and more accurate formula for FG calculation with Refractometer \(Petr Novotny / Zymurgy\), also shows calculated Plato, ABV and ABW
* Added button to save a batch recipe to recipes, overwriting the recipes copy of the recipe, placed next to the update button in the planning tab
* Now lists all ingredients not found in inventory in the planning tab of the batch, click to add it to inventory
* Added **HLT deadspace volume** field to equipment profile, this volume is added to the sparge water amount in the water calculator
* Shorter recipe share URL \(**share.brewfather.app/id**\), old URL still works
* Show warning when mash water/volume limit is exceeded
* Added more icons to top toolbar of recipe and batch when in desktop mode
* Added user note field to all ingredients/inventory
* Added Hopcat / Brew Monk 50L equipment profile
* Now shows recipe in completed tab of batch
* Minor visual changes

### Fixed

* Fixed an issue where a few ingredients did not get the stock from inventory in planning tab batch inventory list
* No longer play notification/alarm right after opening the app if a brew tracker was active before app was shut down

## 1.1.18 - 17.08.2018

### Fixed

* Fixed an issue where water profiles that did not have a type \(source/target\) defined did not show

## 1.1.17 - 16.08.2018

### Features

* Brew Timer
* Brewers Association 2018 Style Guidelines \(Complete\)
* BJCP Mead Style Guidelines
* BJCP Cider Style Guidelines
* Click the version number to open the change log \(this page\)

### Added

* A more stringent way to change batch status
* Now logs when batch status has changed to the log
* Sparge Temperature can be set in the Equipment Profile
* Carbonation calculator: Added Corn Sugar and DME
* Polyclar Brewbrite fining as Misc
* More Norwegian Farmhouse Kveiks \(Yeasts\)
* Beer Brew 30 and Beer Brew 60 equipment profiles
* Added Grain Temp as separate temperature for strike temp calculation
* Adde type to water profile: Source or Target
* A few more water profiles added

### Fixed

* Fixed Norbrygg styles with no maximum OG
* No longer show brew button in batch recipe mode
* Water calculator now shows if you entered 0 as mash/sparge volume
* Now handles special characters in BeerXML export
* Sorting order of day x dry hops

## 1.1.16 - 31.07.2018

### Added

* Option to select Cubic \(default\) or Linear formula in the refractometer tool when calculating your FG of fermented wort. Linear formula works better i.e. if you have a high gravity beer with high \(&gt;1.022\) expected FG.

### Fixed

* Fixed an issue where editing "next batch number" in Settings would cause your next batch number to increment like a string, and logging with Tilt to a batch created after this would not work unless you edit the batch number manually in the batch after creating it.

## 1.1.15 - 28.07.2018

### Added

* Added Mangrove Jaks's M41 Belgian Ale Yeast
* Added OG and FG range description for fermented wort calculation in refractometer tool

### Changed

* Set 1,04 as default refractometer factor

### Fixed

* BH Efficiency not showing for batches created prior to v 1.1.14

## 1.1.14 - 27.07.2018

### Features

* Include grain volume in mash limit \(optional in the equipment profile\)
* Shows Post-boil Gravity when it is different from the Original Gravity - also as a field when logging your batch
* Added option to select "day x" or "x days" \(default\) when adding Dry Hop
* When selecting First Wort Hop time will default to the equipment profile boil time \(if time is 0/blank it will now use the boil time from the equipment profile when calculating IBU\)
* Shows vitals in the style section even if no style is selected
* Larger window for equipment profile on desktop

### New Tools

* Color Converter \([@mattl-nz](https://github.com/mattl-nz)\)
* Refractometer Calibration built into the refractometer tool \([@mattl-nz](https://github.com/mattl-nz)\)

### Fixed

* Fix scaling of fermentables that are not in mash
* Batch number: it is no longer possible to set decimals or batch number below 1
* Bottling temperature now changed to peak fermentation temperature - for calculating priming sugar

## 1.1.13 - 18.07.2018 <a id="coming-soon"></a>

### Features

* Show mash volume \(water + grain\) in recipe
* Show target water profile name in recipe when exists
* Added Safale BE-134, Safale HA-18 yeasts

### Fixed

* Batch recipe could wrongfully update in the old batch if opened in the same session and you changed the same base recipe in a new batch
* Keg \(Force\) carbonation, was giving slightly lower pressure than it was supposed to

## 1.1.12 - 08.07.2018 <a id="coming-soon"></a>

### Features

* **Strike water temperature calculation** in recipe
  * Enable it in your equipment profile \(scroll all the way down\)
  * New fields in equipment profile for room temperature and mash-tun heat capacity
* **Autosave for Recipe** - can be toggled off in settings
* You can now **disable inventory** tracking in settings
* Added Fermentability % field on fermentables, this is used to estimate FG
* Origin as searchable field in fermentables
* Show "Set" when FG is set manually \(default when imported\)
* Set 23L as max mash water limit on the default GF profiles, to prevent too much mash water on big batches
* Added calibration temp as field in hydrometer correction tool
* Added calibration factor in the refractometer tool
* Round to nearest gram rather than nearest 10 grams in fermentables when scaling recipes, works better when scaling to very small batches

### New Tools

* Strike/infusion Water Temperature Calculator
* Rest-step Temperature Calculator
* Mash-Tun Calibration Tool - to find your mash-tun heat capacity

### Fixed

* Remove MashTunDeadSpace in no-sparge mash-water formula
* Fixed RO-water profile
* Fixed WB-06 yeast attenuation

## 1.1.11 - 01.07.2018 <a id="coming-soon"></a>

### Fixed

* Corrected auto calculation of efficiencies when using **Kettle** as batch volume target
* Now includes Mas-Tun Loss in efficiencies calculation

## 1.1.10 - 01.07.2018 <a id="coming-soon"></a>

### Fixed

* Corrected Pre-Boil Gravity calculation when using **Kettle** as batch volume target
* Corrected Decoction misspelling

## 1.1.9 - 25.06.2018 <a id="coming-soon"></a>

### Features

* Added Cryo as Hop form
* Added Water limits on equipment profile
  * Max and min limit for mash water amount
  * Max limit for sparge water
* Added equipment profiles for **Speidel Braumeister 50L / 20L / 10L**
  *  These will give correct mash water amount based on the official recommendation of mash water amount.
* Added Help button in menu which will open the docs

### Fixed

* Fixed hop total amount not updated on delete

### Changes

* Adjusted lactic acid strengt as mash addition, is now approximately 30% stronger, meaning your amount will be about 30% less at same estimated pH.

While some have reported very close to reported pH after lactic acid addition there has also been a number of reports on the amount being too high and giving a lower than estimated pH, still looking for feedback on this, **please report your results**.

## 1.1.7 - 22.06.2018 <a id="coming-soon"></a>

### Features

* Added grain category in fermentables for grains, used in water calculator and FG estimation. If left blank it will be set automatically based on name and color
* Improved FG estimation for Munich base malt

### Fixed

* Yeast calculator \(only when opened from recipe designer\) giving too high target cell count when using US gal or Imperial gal, now works correctly for all units

## 1.1.6 - 21.06.2018 <a id="coming-soon"></a>

### Features

* Duplicate batch button
* Save button at upper toolbar in desktop mode \(recipe\)
* Update recipe from original recipe in batch
* Color on mash and sparge misc additions in brew-sheet
* Water calculator: If no target is selected AUTO button will make a target based on the selected style \(average of max and min values per mineral\)
* Mash Tun Loss \(Unrecoverable\) as a field in the equipment profile and water formulas
* Improved pre-boil gravity calculation accuracy: Now accounts for boil temperature water density for boil volume
* Button for setting no-sparge formulas in equipment profile

### Fixed

* Batch notes will now sort chronological \(descending\)
* Volume 0 for sparge water in water calculator now handeled correctly
* Carbonation calculator at 0 degrees now works

## 1.1.5 - 15.06.2018 <a id="coming-soon"></a>

### Fixed <a id="fixed"></a>

* Fix month not setting correctly when editing batch note time
* Fix clone/copying recipe not working
* Grains with mash time set did not show in water calculator. Grains with &gt; 20 minutes will now show in water calculator

## 1.1.3 - 14.06.2018

### Features

* Yearly subscription added, if you are already subscribing to the monthly you can upgrade to this, and you will only be billed the difference within the current billing period.
* Import multiple recipes from one BeerXML
* Autosave in batch, \(you can now have the batch open on mobile + desktop at the same time and it should update within seconds on the other screen when you make changes\)
* Hopstand temperature per hop-addition
* Fermenter additions show in fermenter tab in batch
* Add withouth closing \(+ button\) on all ingredients
* Ability to edit/set time of batch note

### Fixed

* Minor fixes to the water calculator

## Older versions

Not documented.

