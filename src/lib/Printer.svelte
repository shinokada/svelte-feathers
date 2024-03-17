<script>
  import { getContext } from 'svelte';
  const ctx = getContext('iconCtx') ?? {};
  export let size = ctx.size || '24';
  export let role = ctx.role || 'img';
  export let color = ctx.color || 'currentColor';
  export let tabIndex = ctx.tabIndex || '-1';
  export let fill = ctx.fill || 'none';
  export let ariaLabel = 'printer';
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
  ><polyline points="6 9 6 2 18 2 18 9" /><path
    d="M6 18H4a2 2 0 0 1-2-2v-5a2 2 0 0 1 2-2h16a2 2 0 0 1 2 2v5a2 2 0 0 1-2 2h-2"
  /><rect x="6" y="14" width="12" height="8" /></svg
>

<!--
@component
[Go to docs](https://svelte-feathers.codewithshin.com)
## Props
@prop export let size = ctx.size || '24';
@prop export let role = ctx.role || 'img';
@prop export let color = ctx.color || 'currentColor';
  export let tabIndex = ctx.tabIndex || '-1';
@prop export let ariaLabel = 'printer';
-->
