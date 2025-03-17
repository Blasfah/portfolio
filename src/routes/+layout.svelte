<script>
  import FancyText from '$lib/components/FancyText.svelte'
  import TitleSection from '$lib/components/TitleSection.svelte'

  let { children } = $props()
</script>

{@render children()}

<footer class="footer">
  <div class="footer-section">
    <TitleSection title="find me on">
      <div class="footer-items">
        <FancyText text="Github" />
        <FancyText text="LinkedIn" />
      </div>
    </TitleSection>
  </div>
  <div class="footer-section">
    <TitleSection title="get in touch">
      <div class="footer-items">
        <FancyText text="WouterKuyt@<wbr/>gmail.com" />
        <FancyText text="+31 6 33 13 67 86" />
      </div>
    </TitleSection>
  </div>
</footer>

<style>
  .footer {
    display: flex;
    width: 100%;
    padding-bottom: var(--spacing-medium);
    margin-top: var(--spacing-ultra);
    gap: var(--spacing-large);
  }
  .footer-section {
    flex-grow: 1;
  }
  .footer-items {
    font-size: var(--text-large);
    display: flex;
    flex-direction: column;
    gap: var(--spacing-small);
  }

  @media (max-width: 1440px) {
    .footer-items {
      font-size: var(--text-medium);
    }
  }

  @media (max-width: 1024px) {
    .footer {
      gap: var(--spacing-medium);
      margin-top: var(--spacing-mega);
    }
  }

  @media (max-width: 768px) {
    .footer {
      gap: var(--spacing-large);
      padding-bottom: var(--spacing-small);
      flex-direction: column;
    }
  }
</style>
