<h1 align="center">Svelte Feathers</h1>

<p align="center">
<a href="https://svelte-feathers.codewithshin.com/">Svelte-Feathers</a>
</p>

<p align="center">
<a href="https://github.com/sponsors/shinokada" target="_blank"><img src="https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86" height="25"></a>
<a href="https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps" target="_blank"><img src="https://img.shields.io/badge/PWA-enabled-brightgreen" alt="PWA Shield" height="25">
</a>
<a href="https://www.npmjs.com/package/svelte-feathers" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/v/svelte-feathers" alt="npm" height="25"></a>
<a href="https://twitter.com/shinokada" rel="nofollow" target="_blank"><img src="https://img.shields.io/badge/created%20by-@shinokada-4BBAAB.svg" alt="Created by Shin Okada" height="25"></a>
<a href="https://opensource.org/licenses/MIT" rel="nofollow" target="_blank"><img src="https://img.shields.io/github/license/shinokada/svelte-feathers" alt="License" height="25"></a>
<a href="https://www.npmjs.com/package/svelte-feathers" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/dw/svelte-feathers.svg" alt="npm" height="25"></a>
</p>

Svelte-Feathers is a collection of simply beautiful open source icons for Sveltejs. Each icon is designed on a 24x24 grid with an emphasis on simplicity, consistency and readability. All icons support major CSS frameworks.

<p align="center">
<img width="650" src="/static/images/feather-optimized.png" />
</p>

## Installation new

```sh
npm i -D svelte-feathers
```

## Icon list

Please see this [Icon names](/icon-list.md).

## Usage

```html
<script>
import { ActivityIcon, AirplayIcon } from 'svelte-feathers';
</script>

<ActivityIcon color="#c61515" size="12" />

<AirplayIcon color="#23deff" size="36" />
```


## Faster compiling

For faster compilation, you can import the icon directly.

```html
<script>
  import ActivityIcon from 'svelte-feathers/ActivityIcon.svelte';
</script>

<Us />
```

If you are TypeScript user, **this require `"typescript": "^5.0.0"`.**

As of March 2023, the `typescript@beta` version is now available:

```sh
pnpm i -D typescript@beta
```

To avoid any complaints from the editor, add `node16` or `nodenext` to `moduleResolution` in your tsconfig.json file.

```json
{
  //...
  "compilerOptions": {
    // ...
    "moduleResolution": "nodenext"
  }
}
```

## REPL

[REPL](https://svelte.dev/repl/1fe15642604f48b38e2ea67ead9818dc?version=3.47.0)

[REPL](https://svelte.dev/repl/a759c2c6f2f94c0f8a2d07b1889b2faf?version=3.47.0)

## Size

Use the size prop to change the size of icons.

```html
<UnlockIcon size="24" />
```

## CSS HEX Colors

Use the color prop to change colors with HEX color code.

```html
<UnlockIcon color="#6dff6b" />
```

## CSS frameworks support

Use the class prop to change size, colors and add additional css.

Tailwind CSS example:

```html
<UnlockIcon class="h-24 w-24 text-blue-700 mr-4" />
```

Bootstrap example:

```html
<UnlockIcon class="position-absolute top-0 px-1" />
```

## Import all

You can also include the whole icon pack:

```html
<script>
import * as Icon from 'svelte-feathers';
</script>

<UnlockIcon color="#6dff6b" size="24" />
```

## Unfocusable icon

If you want to make an icon unfocusable, add `tabindex="-1"`.

```html
<UnlockIcon tabindex="-1" />
```

## Passing down other attributes

You can pass other attibutes as well.

```html
<UnlockIcon tabindex="0" />
```

## Using svelte:component

```html
<script>
  import { UnlockIcon } from 'svelte-feathers';
</script>

<svelte:component this="{UnlockIcon}" />
```

## Using onMount

```html
<script>
  import { UnlockIcon } from 'svelte-feathers';
  import { onMount } from 'svelte';
  const props = {
    size: '50',
    color: '#ff0000'
  };
  onMount(() => {
    const icon = new UnlockIcon({ target: document.body, props });
  });
</script>
```

## Based on Feather Icons  ```v4.29.0```

https://feathericons.com/

## Other icons

- [Svelte-Icon-Sets](https://svelte-svg-icons.vercel.app/)

## PWA: Fast & Offline

This website can be downloaded and installed on your device for offline access as a Progressive Web App.

To install a PWA, look for the "Add to Home Screen" option in the browser's menu or settings. On most mobile devices, this option can be found by visiting the website, then selecting the "Options" or "Menu" button in the browser, and looking for the "Add to Home Screen" option. On some desktop browsers, right-click on the page and select "Install".
