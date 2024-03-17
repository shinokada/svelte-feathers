<script>
  import { getContext } from 'svelte';
  const ctx = getContext('iconCtx') ?? {};
  export let size = ctx.size || '24';
  export let role = ctx.role || 'img';
  export let color = ctx.color || 'currentColor';
  export let tabIndex = ctx.tabIndex || '-1';
  export let fill = ctx.fill || 'none';
  export let ariaLabel = 'cloud drizzle';
</script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  viewBox="0 0 24 24"
  fill={fill}
  stroke={color}
  tabIndex={tabIndex}
  stroke-width="2"
  stroke-linecap="round"
  stroke-linejoin="round"
  class={$$props.class}
  {role}
  aria-label={ariaLabel}
  on:click
  on:keydown
  on:keyup
  on:focus
  on:blur
  on:mouseenter
  on:mouseleave
  on:mouseover
  on:mouseout
  ><line x1="8" y1="19" x2="8" y2="21" /><line x1="8" y1="13" x2="8" y2="15" /><line
    x1="16"
    y1="19"
    x2="16"
    y2="21"
  /><line x1="16" y1="13" x2="16" y2="15" /><line x1="12" y1="21" x2="12" y2="23" /><line
    x1="12"
    y1="15"
    x2="12"
    y2="17"
  /><path d="M20 16.58A5 5 0 0 0 18 7h-1.26A8 8 0 1 0 4 15.25" /></svg
>

<!--
@component
[Go to docs](https://svelte-feathers.codewithshin.com)
## Props
@prop export let size = ctx.size || '24';
@prop export let role = ctx.role || 'img';
@prop export let color = ctx.color || 'currentColor';
  export let tabIndex = ctx.tabIndex || '-1';
@prop export let ariaLabel = 'cloud drizzle';
-->
