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
  export let ariaLabel = 'dribbble';
</script>

{#if withEvents}
  <svg
    xmlns="http://www.w3.org/2000/svg"
    width={size}
    height={size}
    viewBox="0 0 24 24"
    {...$$restProps}
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
    <circle cx="12" cy="12" r="10" /><path
      d="M8.56 2.75c4.37 6.03 6.02 9.42 8.03 17.72m2.54-15.38c-3.72 4.35-8.94 5.66-16.88 5.85m19.5 1.9c-3.5-.93-6.63-.82-8.94 0-2.58.92-5.01 2.86-7.44 6.32"
    />
  </svg>
{:else}
  <svg
    xmlns="http://www.w3.org/2000/svg"
    width={size}
    height={size}
    viewBox="0 0 24 24"
    {...$$restProps}
    stroke={color}
    stroke-width="2"
    stroke-linecap="round"
    stroke-linejoin="round"
    class={className}
    {role}
    aria-label={ariaLabel}
  >
    <circle cx="12" cy="12" r="10" /><path
      d="M8.56 2.75c4.37 6.03 6.02 9.42 8.03 17.72m2.54-15.38c-3.72 4.35-8.94 5.66-16.88 5.85m19.5 1.9c-3.5-.93-6.63-.82-8.94 0-2.58.92-5.01 2.86-7.44 6.32"
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
@prop export let ariaLabel = 'dribbble';
-->
