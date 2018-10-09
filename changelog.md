# Changelog

## In developement / Coming soon {#coming-soon}

[Visit the issue tracker for more info](https://bitbucket.org/brewfather/brewfather/issues?&sort=-votes).

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

## 1.1.13 - 18.07.2018 {#coming-soon}

### Features

* Show mash volume \(water + grain\) in recipe
* Show target water profile name in recipe when exists
* Added Safale BE-134, Safale HA-18 yeasts

### Fixed

* Batch recipe could wrongfully update in the old batch if opened in the same session and you changed the same base recipe in a new batch
* Keg \(Force\) carbonation, was giving slightly lower pressure than it was supposed to

## 1.1.12 - 08.07.2018 {#coming-soon}

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

## 1.1.11 - 01.07.2018 {#coming-soon}

### Fixed

* Corrected auto calculation of efficiencies when using **Kettle** as batch volume target
* Now includes Mas-Tun Loss in efficiencies calculation

## 1.1.10 - 01.07.2018 {#coming-soon}

### Fixed

* Corrected Pre-Boil Gravity calculation when using **Kettle** as batch volume target
* Corrected Decoction misspelling

## 1.1.9 - 25.06.2018 {#coming-soon}

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

## 1.1.7 - 22.06.2018 {#coming-soon}

### Features

* Added grain category in fermentables for grains, used in water calculator and FG estimation. If left blank it will be set automatically based on name and color
* Improved FG estimation for Munich base malt

### Fixed

* Yeast calculator \(only when opened from recipe designer\) giving too high target cell count when using US gal or Imperial gal, now works correctly for all units

## 1.1.6 - 21.06.2018 {#coming-soon}

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

## 1.1.5 - 15.06.2018 {#coming-soon}

### Fixed {#fixed}

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

