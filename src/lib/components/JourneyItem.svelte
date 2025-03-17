<script>
  import FancyText from '$lib/components/FancyText.svelte'

  let { href, name, year, children } = $props()
</script>

<div class="journey-item">
  <div class="name">
    <FancyText {href} text={name} />
  </div>
  <div class="divider">
    <div class="line"></div>
    <p class="date">{year}</p>
  </div>
  <p class="text">
    {@render children()}
  </p>
</div>

<style>
  .journey-item {
    flex-grow: 1;
  }
  .divider {
    display: flex;
    align-items: center;
    gap: var(--spacing-small);
    margin-top: var(--spacing-small);
  }
  .line {
    display: block;
    flex-grow: 1;
    height: 4px;
    background: var(--main-color);
  }
  .name {
    font-size: var(--text-large);
  }
  .text {
    margin-top: var(--spacing-medium);
    line-height: 1.5;
    text-align: justify;
  }

  @media (max-width: 768px) {
    .name {
      font-size: var(--text-medium);
      margin-top: var(--spacing-small);
    }
    .text {
      margin: var(--spacing-small) 0;
    }
  }
</style>
