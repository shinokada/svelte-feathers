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
  export let ariaLabel = 'loader';
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
    <line x1="12" y1="2" x2="12" y2="6" /><line x1="12" y1="18" x2="12" y2="22" /><line
      x1="4.93"
      y1="4.93"
      x2="7.76"
      y2="7.76"
    /><line x1="16.24" y1="16.24" x2="19.07" y2="19.07" /><line
      x1="2"
      y1="12"
      x2="6"
      y2="12"
    /><line x1="18" y1="12" x2="22" y2="12" /><line
      x1="4.93"
      y1="19.07"
      x2="7.76"
      y2="16.24"
    /><line x1="16.24" y1="7.76" x2="19.07" y2="4.93" />
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
    <line x1="12" y1="2" x2="12" y2="6" /><line x1="12" y1="18" x2="12" y2="22" /><line
      x1="4.93"
      y1="4.93"
      x2="7.76"
      y2="7.76"
    /><line x1="16.24" y1="16.24" x2="19.07" y2="19.07" /><line
      x1="2"
      y1="12"
      x2="6"
      y2="12"
    /><line x1="18" y1="12" x2="22" y2="12" /><line
      x1="4.93"
      y1="19.07"
      x2="7.76"
      y2="16.24"
    /><line x1="16.24" y1="7.76" x2="19.07" y2="4.93" />
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
@prop export let ariaLabel = 'loader';
-->
