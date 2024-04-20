<script>
  export let size = "large";
  export let shadow = false;
</script>

<button class={size === "small" ? "size-sm" : "size-lg"}
  ><slot name="btn-text">Fallback Text</slot></button
>

<style lang="scss">
  button {
    background: salmon;
    color: white;
    &.size-sm {
      padding: 0.5rem 1rem;
    }
    &.size-lg {
      padding: 1rem 2rem;
      font-size: 20px;
    }
  }
</style>
