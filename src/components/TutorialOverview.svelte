<script>
  /**
   * @type {{text: string, slug: string}[]}
   */
  export let items;
</script>

{#if items && items.length > 0}
  <section class="tutorial-overview">
    <h2 class="overview-header">What You'll Learn</h2>
    <ol class="overview-list">
      {#each items as item}
        <li class="overview-item">
          <a href="#{item.slug}" class="overview-link">{item.text}</a>
        </li>
      {/each}
    </ol>
    <slot />
  </section>
{/if}

<style>
  .tutorial-overview {
    background: var(--background-muted);
    padding: var(--space-2xs-xs);
  }
  .overview-header {
    font-size: var(--step-0);
  }
  .overview-list {
    padding-inline-start: 1.5em;
  }
  .overview-item {
    font-size: var(--step--1);
    letter-spacing: 0.05em;
  }
</style>
