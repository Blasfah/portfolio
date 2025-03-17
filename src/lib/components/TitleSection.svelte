<script>
  let { children, title } = $props()
</script>

<section class="title-section">
  <h2 class="title">{title}</h2>
  <span class="divider"></span>
  <div class="content">
    {@render children()}
  </div>
</section>

<style>
  .title-section {
    width: 100%;
  }
  .title {
    font-size: var(--text-medium);
  }
  .divider {
    display: block;
    width: 100%;
    height: 4px;
    background: var(--main-color);
    margin-top: var(--spacing-medium);
  }
  .content {
    margin-top: var(--spacing-medium);
  }

  @media (max-width: 768px) {
    .title {
      font-size: var(--text-small);
    }
    .divider {
      margin-top: var(--spacing-small);
    }
    .content {
      margin-top: var(--spacing-small);
    }
  }
</style>
