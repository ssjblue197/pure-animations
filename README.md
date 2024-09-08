# Pure UI Animations

Your favorite [animate.css](https://animate.style/) effects available as ES modules for use with the [Web Animations API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Animations_API).

- 🏆 ~100 quality animations
- 🎾 ~30 popular easings
- 🚚 Works with CDNs
- 🌲 Fully tree-shakeable


This module was built for [Pure UI](https://pureui.xyz/), but it works well as a stand-alone library too!

## Installation

```bash
npm install pure-animations
```

## Usage

Importing all animations:

```js
import * as animations from 'pure-animations';
```

Importing individual animations:

```js
import { bounce } from 'pure-animations';
```

Importing easings:

```js
import { easings } from 'pure-animations';
```

Animating an element:

```html
<div style="display: block; width: 100px; height: 100px; background: tomato; margin: 2rem;"></div>

<script type="module">
  import { easings, flip } from 'https://cdn.jsdelivr.net/npm/pure-animations@1/dist/index.js';

  const box = document.querySelector('div');

  box.animate(flip, {
    duration: 1500,
    iterations: Infinity,
    easing: easings.easeInSine
  });
</script>
```

This example uses the [jsDelivr CDN](https://www.jsdelivr.com/). To import the library locally, install it and make `node_modules/pure-animations/dist` available to your app or bundler.

## Developers

This script parses all animation stylesheets found in `node_modules/animate.css` and generates [keyframe objects](https://developer.mozilla.org/en-US/docs/Web/API/Web_Animations_API/Keyframe_Formats) that you can use with the [Web Animations API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Animations_API). As animations are tweaked and added to animate.css, the keyframes herein will be kept in sync when rerunning the script.

To build the project, run:

```bash
npm run build
```

This will purge and rebuild the `dist` directory.

Please report all bugs and suggestions to [the issue tracker](https://github.com/ssjblue197/pure-animations/issues).
# pure-animations
