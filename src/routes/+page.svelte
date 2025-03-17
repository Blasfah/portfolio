<script>
  import FancyText from '$lib/components/FancyText.svelte'
  import JourneyItem from '$lib/components/JourneyItem.svelte'
  import TitleSection from '$lib/components/TitleSection.svelte'
</script>

<section class="section-full">
  <nav class="nav">
    <FancyText href="https://www.wouterkuyt.nl/" text="Wouter Kuyt" />
    <h1>Portfolio</h1>
  </nav>
  <div class="header">
    <TitleSection title="Introduction">
      <h1 class="text">
        Hi! - I'm Wouter Kuyt, a GLR graduate born in 2003 and a front-end
        fanatic who loves building stunning, user-friendly websites.
      </h1>
    </TitleSection>
  </div>
</section>
<section class="section-page">
  <div class="text-center">
    <p class="journey-text">
      Here, you'll find all the great places I've worked at, my experience
      there, and the skills I've gained along the way. <span class="red-text"
        >Could your company be next?</span
      >
    </p>
  </div>
</section>
<section class="section-page">
  <div class="journey">
    <JourneyItem
      href="https://www.pixeldeluxe.nl/"
      name="PixelDeluxe"
      year="2022"
    >
      Working at PixelDeluxe as an intern was my first experience with working
      full-time. I worked here with CraftCMS and TailwindCSS, both of which I
      loved working with. I had a great time here and even stayed for an 2 extra
      days!
    </JourneyItem>
    <JourneyItem href="https://www.ara.nl/nl" name="ARA" year="2023">
      ARA was my second intership, but definitely not the second in experience!
      I got to work on their own website, cool animations and last but not least
      the all-powerfull meta-framework Next.js! Also very fond of the warm
      chocolate there.
    </JourneyItem>
    <JourneyItem href="https://www.radancy.com/nl/" name="Radancy" year="2024">
      My first real job, made me realize there is still so much more to learn.
      At Radancy I worked on a variety of different things ranging from
      ad-banners to library components. I worked on websites of some very big
      partners and got to see how these giant and demanding websites make it all
      happen!
    </JourneyItem>
  </div>
</section>

<style>
  .nav {
    display: flex;
    justify-content: space-between;
  }
  .section-full {
    height: 100vh;
    display: flex;
    flex-direction: column;
    padding-top: var(--spacing-medium);
  }
  .section-page {
    margin-top: var(--spacing-medium);
  }
  .header {
    display: flex;
    flex-grow: 1;
    align-items: center;
  }
  .text {
    line-height: 1.2;
    font-size: var(--text-large);
    text-align: justify;
  }
  .text-center {
    display: flex;
    justify-content: center;
  }
  .journey-text {
    font-size: var(--text-medium);
    max-width: var(--text-max-width);
    line-height: 1.5;
  }
  .journey {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    column-gap: var(--spacing-large);
    row-gap: var(--spacing-mega);
    margin-top: var(--spacing-mega);
  }
  .red-text {
    color: var(--main-color);
  }

  @media (max-width: 1024px) {
    .text {
      font-size: var(--text-medium);
    }
    .section-full {
      padding-top: var(--spacing-small);
    }
    .journey {
      grid-template-columns: 1fr;
    }
  }

  @media (max-width: 768px) {
    .text {
      text-align: initial;
      line-height: 1.5;
    }
    .journey {
      gap: var(--spacing-medium);
    }
  }
</style>
