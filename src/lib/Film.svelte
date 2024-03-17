<script>
  import { getContext } from 'svelte';
  const ctx = getContext('iconCtx') ?? {};
  export let size = ctx.size || '24';
  export let role = ctx.role || 'img';
  export let color = ctx.color || 'currentColor';
  export let tabIndex = ctx.tabIndex || '-1';
  export let fill = ctx.fill || 'none';
  export let ariaLabel = 'film';
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
  ><rect x="2" y="2" width="20" height="20" rx="2.18" ry="2.18" /><line
    x1="7"
    y1="2"
    x2="7"
    y2="22"
  /><line x1="17" y1="2" x2="17" y2="22" /><line x1="2" y1="12" x2="22" y2="12" /><line
    x1="2"
    y1="7"
    x2="7"
    y2="7"
  /><line x1="2" y1="17" x2="7" y2="17" /><line x1="17" y1="17" x2="22" y2="17" /><line
    x1="17"
    y1="7"
    x2="22"
    y2="7"
  /></svg
>

<!--
@component
[Go to docs](https://svelte-feathers.codewithshin.com)
## Props
@prop export let size = ctx.size || '24';
@prop export let role = ctx.role || 'img';
@prop export let color = ctx.color || 'currentColor';
  export let tabIndex = ctx.tabIndex || '-1';
@prop export let ariaLabel = 'film';
-->
