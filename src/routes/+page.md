# Svelte Feathers

<div class="flex gap-2 my-8">
<a href="https://github.com/sponsors/shinokada" target="_blank"><img src="https://img.shields.io/static/v1?label=Sponsor&message=%E2%9D%A4&logo=GitHub&color=%23fe8e86" alt="sponsor" height="25"></a>
<a href="https://www.npmjs.com/package/svelte-feathers" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/v/svelte-feathers" alt="npm" height="25"></a>
<a href="https://twitter.com/shinokada" rel="nofollow" target="_blank"><img src="https://img.shields.io/badge/created%20by-@shinokada-4BBAAB.svg" alt="Created by Shin Okada" height="25"></a>
<a href="https://opensource.org/licenses/MIT" rel="nofollow" target="_blank"><img src="https://img.shields.io/github/license/shinokada/svelte-feathers" alt="License" height="25"></a>
<a href="https://www.npmjs.com/package/svelte-feathers" rel="nofollow" target="_blank"><img src="https://img.shields.io/npm/dw/svelte-feathers.svg" alt="npm" height="25"></a>
</div>

280+ Svelte-Feathers icon components for Svelte. It is a collection of simply beautiful open source icons for Sveltejs. Each icon is designed on a 24x24 grid with an emphasis on simplicity, consistency and readability.

Thank you for considering my open-source package. If you use it in a commercial project, please support me by sponsoring me on GitHub: https://github.com/sponsors/shinokada. Your support helps me maintain and improve this package for the benefit of the community.

## Installation

```sh
pnpm i -D svelte-feathers
```

## Repo

[GitHub Repo](https://github.com/shinokada/svelte-feathers)

## Original source

[feathericons/feather](https://github.com/feathericons/feather)

## License

[Svelte-Feathers License](https://github.com/shinokada/svelte-feathers/LICENSE)

[feathericons/feather License](https://github.com/feathericons/feather/blob/master/LICENSE)


## Usage

```html
<script>
  import { ActivityIcon, AirplayIcon } from 'svelte-feathers';
</script>

<ActivityIcon color="#c61515" size="12" />

<AirplayIcon color="#23deff" size="36" />
```

## Faster compiling

If you need only a few icons from this library in your Svelte app, import them directly. This can optimize compilation speed and improve performance by reducing the amount of code processed during compilation.

```html
<script>
  import ActivityIcon from 'svelte-feathers/ActivityIcon.svelte';
</script>

<ActivityIcon />
```

If you are a TypeScript user, install **typescript version 5.0.0 or above**.

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

## Props

- size = '24';
- color = 'currentColor';
- role = 'img';

## IDE support

If you are using an LSP-compatible editor, such as VSCode, Atom, Sublime Text, or Neovim, hovering over a component name will display a documentation link, props, and events.

## Size

Use the size prop to change the size of icons.

```html
<UnlockIcon size="24" />
```

If you are using Tailwind CSS, you can add a custom size using Tailwind CSS by including the desired classes in the class prop. For example:

```html
<UnlockIcon class="shrink-0 h-20 w-20" />
```

## CSS HEX Colors

Use the color prop to change colors with HEX color code.

```html
<UnlockIcon color="#6dff6b" />
```

## CSS frameworks support

You can apply CSS framework color and other attributes directly to the icon component or its parent tag using the class prop.

Tailwind CSS example:

```html
<UnlockIcon class="h-24 w-24 text-blue-700 mr-4" />
```

Bootstrap example:

```html
<UnlockIcon class="position-absolute top-0 px-1" />
```

Dark mode with Tailwind CSS
If you are using the dark mode on your website with Tailwind CSS, add your dark mode class to the class prop.

Let’s use dark for the dark mode class as an example.

```html
<script>
  import { UnlockIcon } from 'svelte-feathers';
</script>

<UnlockIcon class="text-blue-700 dark:text-red-500" />
```

## Unfocusable icon

If you want to make an icon unfocusable, add `tabindex="-1"`.

```html
<UnlockIcon tabindex="-1" />
```

## Event

All icons have the following events:

- on:click
- on:keydown
- on:keyup
- on:focus
- on:blur
- on:mouseenter
- on:mouseleave
- on:mouseover
- on:mouseout

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

## Import all

You can also include the whole icon pack:

```html
<script>
  import * as Icon from 'svelte-feathers';
</script>

<UnlockIcon color="#6dff6b" size="24" />
```

## Other icons

[Svelte-Icon-Sets](https://svelte-svg-icons.vercel.app/)
