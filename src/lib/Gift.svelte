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
  export let ariaLabel = 'gift';
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
    <polyline points="20 12 20 22 4 22 4 12" /><rect x="2" y="7" width="20" height="5" /><line
      x1="12"
      y1="22"
      x2="12"
      y2="7"
    /><path d="M12 7H7.5a2.5 2.5 0 0 1 0-5C11 2 12 7 12 7z" /><path
      d="M12 7h4.5a2.5 2.5 0 0 0 0-5C13 2 12 7 12 7z"
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
    <polyline points="20 12 20 22 4 22 4 12" /><rect x="2" y="7" width="20" height="5" /><line
      x1="12"
      y1="22"
      x2="12"
      y2="7"
    /><path d="M12 7H7.5a2.5 2.5 0 0 1 0-5C11 2 12 7 12 7z" /><path
      d="M12 7h4.5a2.5 2.5 0 0 0 0-5C13 2 12 7 12 7z"
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
@prop export let ariaLabel = 'gift';
-->
