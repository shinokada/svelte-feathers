<script lang="ts">
  import { getContext } from 'svelte';
  interface CtxType {
    size?: string;
    withEvents?: boolean;
    role?: string;
    color?: string;
    class?: string;
  }
  const ctx: CtxType = getContext('iconCtx') ?? {};
  interface Props {
    size?: string;
    withEvents?: boolean;
    role?: string;
    color?: string;
    ariaLabel?: string;
    class?: string;
  }
  let className = ctx.class || '';
  export { className as class };
  export let size = ctx.size || '24';
  export let withEvents: boolean = false;
  export let role = ctx.role || 'img';
  export let color = ctx.color || 'currentColor';
  export let ariaLabel = 'tag';
</script>

{#if withEvents}
  <svg
    xmlns="http://www.w3.org/2000/svg"
    width={size}
    height={size}
    viewBox="0 0 24 24"
    {...$$restProps}
    fill="none"
    stroke={color}
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    class={className}
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
  >
    <path d="M20.59 13.41l-7.17 7.17a2 2 0 0 1-2.83 0L2 12V2h10l8.59 8.59a2 2 0 0 1 0 2.82z" /><line
      x1="7"
      y1="7"
      x2="7.01"
      y2="7"
    />
  </svg>
{:else}
  <svg
    xmlns="http://www.w3.org/2000/svg"
    width={size}
    height={size}
    viewBox="0 0 24 24"
    {...$$restProps}
    fill="none"
    stroke={color}
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    class={className}
    {role}
    aria-label={ariaLabel}
  >
    <path d="M20.59 13.41l-7.17 7.17a2 2 0 0 1-2.83 0L2 12V2h10l8.59 8.59a2 2 0 0 1 0 2.82z" /><line
      x1="7"
      y1="7"
      x2="7.01"
      y2="7"
    />
  </svg>
{/if}

<!--
@component
[Go to docs](https://svelte-feathers.codewithshin.com)
## Props
@prop export let size = ctx.size || '24';
@prop export let withEvents: boolean = false;
@prop export let role = ctx.role || 'img';
@prop export let color = ctx.color || 'currentColor';
@prop export let ariaLabel = 'tag';
-->
