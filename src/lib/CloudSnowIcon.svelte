<script>
  export let size = '24';
  export let role = 'img';
  export let color = 'currentColor';
</script>

<svg
  xmlns="http://www.w3.org/2000/svg"
  width={size}
  height={size}
  viewBox="0 0 24 24"
  fill="none"
  stroke={color}
  stroke-width="2"
  stroke-linecap="round"
  stroke-linejoin="round"
  class={$$props.class}
  {role}
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
  <path d="M20 17.58A5 5 0 0 0 18 8h-1.26A8 8 0 1 0 4 16.25" />
  <line x1="8" y1="16" x2="8.01" y2="16" />
  <line x1="8" y1="20" x2="8.01" y2="20" />
  <line x1="12" y1="18" x2="12.01" y2="18" />
  <line x1="12" y1="22" x2="12.01" y2="22" />
  <line x1="16" y1="16" x2="16.01" y2="16" />
  <line x1="16" y1="20" x2="16.01" y2="20" />
</svg>

<!--
@component
[Go to Document](https://svelte-feathers.codewithshin.com/)
## Props
@prop size = '24';
@prop role = 'img';
@prop color = 'currentColor';
## Event
- on:click
- on:keydown
- on:keyup
- on:focus
- on:blur
- on:mouseenter
- on:mouseleave
- on:mouseover
- on:mouseout
-->
