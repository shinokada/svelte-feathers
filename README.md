## Svelte-Feathericons

[![npm version](https://badgen.net/npm/v/@codewithshin/svelte-feathericons)](https://www.npmjs.com/package/@codewithshin/svelte-feathericons)
[![license](https://badgen.net/npm/license/@codewithshin/svelte-feathericons)](https://github.com/shinokada/svelte-feathericons/blob/main/LICENSE)

#### What is svelte-feathericons?

svelte-feather is a collection of simply beautiful open source icons for Sveltejs. Each icon is designed on a 24x24 grid with an emphasis on simplicity, consistency and readability.

#### Based on Feather Icons  ```v4.29.0```
https://feathericons.com/

### Installation

```sh
npm i -D @codewithshin/svelte-feathericons
```

### Usage

```html
<script>
import { ActivityIcon, AirplayIcon } from '@codewithshin/svelte-feathericons';
</script>

<ActivityIcon color="#c61515" size="12" />

<AirplayIcon color="#23deff" size="36" />
```

You can also include the whole icon pack:

```html
<script>
import * as Icon from '@codewithshin/svelte-feathericons';
</script>

<Icon.UnlockIcon color="#6dff6b" size="24" />
```

## Icon list

Please see this [Icon list](https://github.com/shinokada/svelte-feathericons/blob/main/icon-list.md)