<h1 align="center">Svelte-Feathers</h1>

<p align="center">
<a href="https://svelte-feathers.codewithshin.com/">Svelte-Feathers</a>
</p>

<p align="center">
<a href="https://www.npmjs.com/package/svelte-feathers" rel="nofollow"><img src="https://img.shields.io/npm/v/svelte-feathers" alt="npm"></a>
<a href="https://twitter.com/shinokada" rel="nofollow"><img src="https://img.shields.io/badge/created%20by-@shinokada-4BBAAB.svg" alt="Created by Shin Okada"></a>
<a href="https://opensource.org/licenses/MIT" rel="nofollow"><img src="https://img.shields.io/github/license/shinokada/svelte-feathers" alt="License"></a>
<a href="https://www.npmjs.com/package/svelte-feathers" rel="nofollow"><img src="https://img.shields.io/npm/dw/svelte-feathers.svg" alt="npm"></a>
</p>

Svelte-Feathers is a collection of simply beautiful open source icons for Sveltejs. Each icon is designed on a 24x24 grid with an emphasis on simplicity, consistency and readability. All icons support major CSS frameworks.

## Installation new

```sh
npm i -D svelte-feathers
```

## Icon list

Please see this [Icon list](https://github.com/shinokada/svelte-feathers/blob/main/icon-list.md)


Here is [Icon names](icon-list.md)

## Usage

```html
<script>
import { ActivityIcon, AirplayIcon } from 'svelte-feathers';
</script>

<ActivityIcon color="#c61515" size="12" />

<AirplayIcon color="#23deff" size="36" />
```

[REPL](https://svelte.dev/repl/1fe15642604f48b38e2ea67ead9818dc?version=3.47.0)

You can also include the whole icon pack:

```html
<script>
import * as Icon from 'svelte-feathers';
</script>

<UnlockIcon color="#6dff6b" size="24" />
```

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

## Based on Feather Icons  ```v4.29.0```

https://feathericons.com/

## Other icons

- [Svelte-Icon-Sets](https://svelte-svg-icons.vercel.app/)