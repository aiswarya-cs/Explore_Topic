<script lang="ts">
  // ✅ Define the shape of your breadcrumb item
  export let items: {
    title: string;
    href?: string;
    active?: boolean;
  }[] = [];
</script>

<nav class="w-full pt-40 text-sm text-muted-foreground">
  <ol class="flex items-center space-x-2">
    {#each items as item, index (item.title)}
      <li class="flex items-center gap-1">
        {#if !item.active}
          <a href={item.href} class="text-[#13547a] text-2xl">{item.title}</a>
        {:else}
          <span class="font-medium text-white text-2xl">{item.title}</span>
        {/if}

        {#if index < items.length - 1}
          <svg
            class="w-4 h-4 mx-1 text-gray-400"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            viewBox="0 0 24 24"
          >
            <path d="M9 5l7 7-7 7" />
          </svg>
        {/if}
      </li>
    {/each}
  </ol>
</nav>
