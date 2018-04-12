# Info

How to convert a component to the new Vue InstantSearch architecture?

1.  copy `/src/components/__Template.vue` to the new component name
1.  follow instructions about modifications inside this file
1.  add the props to the component
1.  add the `widgetParams` based on the props (usually copy-paste)
1.  copy `src/components/__tests__/__template__-test.js` into your own test and edit to fit your usage
1.  run `yarn jest --watch` to run the tests
1.  copy `/stories/__template__.stories.js` into your own story
1.  run `yarn storybook` to see if it works
1. Add docs in `docs/src/components/{name}.md`
1. if it's a new component, also add it in `src/instantsearch.js` (three times)
1. ...
1. Profit!

# Prep work

* [x] pass down an InstantSearch.js instance
* [ ] apply correct properties to the main component
* [x] allow passing of a connector on a widget
* [x] allow destroying of a widget
* [x] allow changing of parameters on a widget
* [x] allow widgetFactories without connector (i.e. `configure`)
* [x] define which options to use
* [x] define which DOM to use
* [ ] update `bem` function to `suit` (CSS)
* [ ] change the way props are passed down with `$props` and filtering out mixin ones

# Components

A checklist for all of the components which are completely done.

x => done
~ => in progress

* [x] `ais-breadcrumb`
* [x] `ais-clear-refinements`
* [x] `ais-configure`
* [x] `ais-current-refinements`
* [x] `ais-hierarchical-menu`
* [ ] `ais-highlight`
* [~] `ais-hits-per-page`
* [ ] `ais-hits`
* [ ] `ais-index`
* [ ] `ais-infinite-hits`
* [ ] `ais-menu-select`
* [ ] `ais-menu`
* [ ] `ais-numeric-menu`
* [ ] `ais-numeric-selector`
* [-] `ais-pagination`
* [ ] `ais-panel`
* [ ] `ais-powered-by`
* [ ] `ais-range-input`
* [ ] `ais-range-slider`
* [ ] `ais-rating-menu`
* [ ] `ais-refinement-list`
* [ ] `ais-search-box`
* [ ] `ais-snippet`
* [ ] `ais-sort-by`
* [ ] `ais-stats`
* [ ] `ais-toggle-refinement`
* [ ] `ais-index`

# Rounding up work

* [ ] release plan
* [ ] migration guide

# Questions/next steps

* [ ] Decides what is provided as state in every widget. Today we get everything without controlling it.
We need to be careful, everything inside state once released will be public API
* [ ] align all filenames to the same convention: Widget.vue, __tests__/Widget.js, stories/Widget.stories.js
