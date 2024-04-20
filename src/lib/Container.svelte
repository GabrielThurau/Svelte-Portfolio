<!-- Container.svelte -->
<div>
  {#if $$slots.header}
    <slot name="header" />
  {/if}
  {#if $$slots.content}
    <slot name="content" />
  {/if}
</div>
<!-- Container.svelte -->
