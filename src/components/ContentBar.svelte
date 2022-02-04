<script>
  import Menu from './Menu.svelte';
  export let titles;
  export let menus;

  console.log(menus);

  menus = menus.map((menu) => {
    return {
      title: titles[menus.indexOf(menu)],
      sections: menu,
    };
  });
</script>

{#each menus as menu, index}
  <details open>
    <summary>
      <span class="summary-inner">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" class="summary-indicator">
          <path fill="none" d="M0 0h24v24H0z" />
          <path d="M13.172 12l-4.95-4.95 1.414-1.414L16 12l-6.364 6.364-1.414-1.414z" />
        </svg>
        <span class="navbar-title">{titles[index]}</span>
      </span>
    </summary>
    <nav class="toc">
      {#each menu.sections as section}
        <ol class="toc-menu" id="navigation">
          <li>
            <a href={section.url}>
              {section.title}
            </a>
          </li>
        </ol>
      {/each}
    </nav>
  </details>
{/each}
