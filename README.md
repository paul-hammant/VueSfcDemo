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

See the diff: [](https://github.com/paul-hammant/VueSfcDemo/commit/)

* velocity-animate referenced in-situ on unpkg rather than from `node_modules/`

## Other changes I made

* Changed from a `document.getElementById()` DOM traversl to a canonicl Vue way (refs)
* component directory reorg: Button feels reusable outside aCalculator so it's loaded as `../Button.vue` now
* Moved velocity-animate logic into the Blinker component from the Display component

## TODO 

* More refactoring.
* Work out how to parameterize velocity-animate version (1.5.2) that's currently hard coded in two places  
* Add Tests