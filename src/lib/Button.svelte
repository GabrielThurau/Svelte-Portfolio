<script>
  export let size = "small";
  export let shadow = false;
</script>

<button class="size-sm"><slot>Fallback Text</slot></button>

<style lang="scss">
  button {
    background: salmon;
    color: white;
    &.size-sm {
      padding: 0.5rem 1rem;
    }
    &.size-lg {
      padding: 1rem 2rem;
    }
  }
</style>
