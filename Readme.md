# Dat Library UI Elements

This is a work in progress.

To do:
[x] Progress Bar
[x] Simple buttons
[x] Dynamic Alerts
[x] Basic Menu (still needs css)
[] Active state for buttons (for selected items)
[] Global Loader
[] Radio Button
[] Basic layout Components (eg sidebar, row, etc)
[] Text inputs
[] Pagination elements
[] Pop up modal
[] Badges (eg. for peer count etc)
[] Accordion Item (for library data)
[] Table structure (for displaying book/author data)
[] ...

You can see all the available components [here](https://e-e-e.github.io/dat-library-ui/).

We are replacing the use of element-ui in [dat library](https://github.com/e-e-e/dat-library).

## Install

```
npm install --save dat-library-ui
```

```js
import Vue from 'vue'
import DatLibraryUI from 'dat-library-ui'
// import styles
import 'dat-library-ui/dist/styles.css'

// injects all components
Vue.use(DatLibraryUI);
```

## Development

```
npm run dev
```

This will create two processes. `Rollup` which will watch and recompile the dat-library-ui bundle, and `Webpack` which launches a sample website at `localhost:8080`. All changes in the src directory will be hot loaded and visible there.

```
npm run build
```

This will rollup the library for production and build new docs representing the changes.



