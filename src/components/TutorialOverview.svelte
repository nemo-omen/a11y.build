<script>
  /**
   * @type {{text: string, slug: string}[]}
   */
  export let items;
</script>

{#if items && items.length > 0}
  <section class="tutorial-overview">
    <h3>What You'll be Learning</h3>
    <ol class="overview-list">
      {#each items as item}
        <li>
          <a href="#{item.slug}">{item.text}</a>
        </li>
      {/each}
    </ol>
    <slot />
  </section>
{/if}
