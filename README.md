[![Build Status](https://travis-ci.org/oaf-project/oaf-bootstrap-4.svg?branch=master)](https://travis-ci.org/oaf-project/oaf-bootstrap-4)
[![npm](https://img.shields.io/npm/v/oaf-bootstrap-4.svg)](https://www.npmjs.com/package/oaf-bootstrap-4)

[![dependencies Status](https://david-dm.org/oaf-project/oaf-bootstrap-4/status.svg)](https://david-dm.org/oaf-project/oaf-bootstrap-4)
[![devDependencies Status](https://david-dm.org/oaf-project/oaf-bootstrap-4/dev-status.svg)](https://david-dm.org/oaf-project/oaf-bootstrap-4?type=dev)
[![peerDependencies Status](https://david-dm.org/oaf-project/oaf-bootstrap-4/peer-status.svg)](https://david-dm.org/oaf-project/oaf-bootstrap-4?type=peer)

# Oaf Bootstrap 4

Accessibility fixes for Bootstrap 4.

## Installation

```sh
# yarn
yarn add --dev oaf-bootstrap-4

# npm
npm install --save-dev oaf-bootstrap-4
```

## Usage

You'll need to recompile Bootstrap's Sass yourself.

Assuming `src/styles/index.scss`:

```scss
// Your Bootstrap variable overrides.
...

// Accessibility fixes that need to come _before_ the Bootstrap import.
@import "../../node_modules/oaf-bootstrap-4/scss/top.scss";

// Bootstrap itself.
@import "../../node_modules/bootstrap/scss/bootstrap.scss";

// Accessibility fixes that need to come _after_ the Bootstrap import.
@import "../../node_modules/oaf-bootstrap-4/scss/bottom.scss";

// Other styles.
...
```

## Fixes

### Restore link underlines

We include a fix for [Bootstrap issue 15304](https://github.com/twbs/bootstrap/issues/15304). That issue is four and a half years old, so don't hold your breath.

From Bootstrap issue 15304:

> For aesthetic reasons, by default Bootstrap links have no underlines, relying instead just on a color difference from surrounding text. This in itself violates WCAG 2.0 "1.4.1 Use of color" http://www.w3.org/TR/WCAG20/#visual-audio-contrast-without-color

### Restore focus outline for tabindex="-1" elements

We include a fix for [Bootstrap issue 28425](https://github.com/twbs/bootstrap/issues/28425).

## See also
* [Bootstrap's Accessibility page](https://getbootstrap.com/docs/4.3/getting-started/accessibility/).
* For a similar library for Bootstrap 3, see [bootstrap-hacks](https://github.com/danielnixon/bootstrap-hacks).
* [Bootstrap accessibility issues](https://github.com/twbs/bootstrap/issues?q=is%3Aissue+is%3Aopen+label%3Aaccessibility).
