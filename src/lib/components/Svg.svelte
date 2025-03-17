<script>
  let { name, width, height } = $props()
</script>

{#if name === 'arrow-down'}
  <svg
    {width}
    {height}
    viewBox="0 -960 960 960"
    fill="currentColor"
    xmlns="http://www.w3.org/2000/svg"
  >
    <path
      d="M440-800v487L216-537l-56 57 320 320 320-320-56-57-224 224v-487h-80Z"
    ></path>
  </svg>
{/if}
