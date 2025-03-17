<script>
  let { text, href = '/#' } = $props()
</script>

<a class="fancy-text" target="_blank" {href}>
  <span class="text-container">
    <span class="text">
      {@html text}
    </span>
    <span class="text reveal">
      {@html text}
    </span>
  </span>
</a>

<style>
  :root {
    --container-gap: 2px;
  }

  .fancy-text,
  .text-container {
    display: inline-flex;
    width: fit-content;
  }

  .text-container {
    position: relative;
    transition: translate 0.25s ease;
    flex-direction: column;
    gap: var(--container-gap);
  }

  .fancy-text {
    overflow: hidden;
  }

  .fancy-text:hover .text-container {
    translate: 0 calc(-100% - var(--container-gap));
  }

  .reveal {
    position: absolute;
    top: calc(100% + var(--container-gap));
    color: var(--main-color);
  }
</style>
