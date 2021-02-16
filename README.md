# VueSfcDemo

Demo of `FranckFreiburger/vue3-sfc-loader` (WIP) For a Calculator SFC demo app

Live Demo: [https://paul-hammant.github.io/VueSfcDemo](https://paul-hammant.github.io/VueSfcDemo/)

## Technologies reused: 

* Nana Kwame Owusu's excellent Calculator SFC demo: [https://github.com/sowusu/VueCalculator](https://github.com/sowusu/VueCalculator). Four components: Calculator, Display, Button, and Blinker.
* Franck Freiburger's [vue3-sfc-loader](https://github.com/FranckFreiburger/vue3-sfc-loader) shim (new version of his existing [http-vue-loader](https://github.com/FranckFreiburger/http-vue-loader) tech)

## Features of this repo/demo

* Buildless
  * no NPM, etc
  * site/app just runs (over http:// and https:// not file://)
* Decomposed solution (Nanas's work, not mine) 

## Changes to get this working with document.getElementById

See the diff: [a0aa20e](https://github.com/paul-hammant/VueSfcDemo/commit/a0aa20e39ba82714d2264ab3efdd4a0a08443a1a) (note Blinker was moved, but Git thinks Added/Deleted - [a feature not a bug](https://stackoverflow.com/questions/433111/how-to-make-git-mark-a-deleted-and-a-new-file-as-a-file-move))

* velocity-animate referenced in-situ on unpkg rather than from `node_modules/`

## Other changes I made

* Changed from a `document.getElementById()` DOM traversl to a canonicl Vue way (refs)
* Component directory reorg: Button feels reusable outside aCalculator so it's loaded as `../Button.vue` now
* Moved velocity-animate logic into the Blinker component from the Display component

## TODO 

* More refactoring. Maybe make Display take some behaviors from Calculator
* Work out how to parameterize velocity-animate version (1.5.2) that's currently hard coded in two places  
* Add Tests
* Work out if there's a one-liner way of injecting a Vue SFC component into a page
  * I wish [HTML imports](https://caniuse.com/imports) was a thing
    
See also: [https://paulhammant.com/2021/02/16/buildless-sfc-vuejs-applications](https://paulhammant.com/2021/02/16/buildless-sfc-vuejs-applications/)