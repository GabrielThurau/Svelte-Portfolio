<script>
  export let size = "large";
  export let shadow = false;
  export let bgColor = "inherit";
  export let txtColor = "inherit";
</script>

<button
  style:--buttonBgColor={bgColor}
  style:--buttonTxtColor={txtColor}
  class:size-lg={size === "large"}
  class:size-sm={size === "small"}
  class:shadow
  class:has-left={$$slots.leftText}
>
  <div class="left-text">
    <slot name="leftText" />
  </div>
  <slot name="btn-text">Fallback Text</slot>
  <slot x="y" />
</button>

<style lang="scss">
  button {
    @mixin flex-center($flex, $alignment) {
      display: $flex;
      align-items: $alignment;
    }
    //display: flex;
    @include flex-center(flex, center);
    background: var(--buttonBgColor);
    color: var(--buttonTxtColor);
    cursor: pointer;
    margin: 0 auto;
    &.has-left > div.left-text {
      margin-right: 1rem;
    }

    &.has-left > div.left-text {
      position: relative;
      top: 3px;
    }

    &:hover {
      background-image: linear-gradient(rgba(0, 0, 0, 0.4) 0 0);
    }
    &:active {
      background-image: linear-gradient(rgba(255, 255, 255, 0.1) 0 0);
    }
    &.size-sm {
      padding: 0.5rem 1rem;
    }
    &.size-lg {
      padding: 1rem 2rem;
      font-size: 20px;
    }
    &.shadow {
      box-shadow: 0 0 10px rgba(1, 1, 1, 0.33);
    }
  }
</style>
