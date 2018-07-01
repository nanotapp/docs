# Changelog

## In developement {#coming-soon}

### Features

* Brew Timer

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

