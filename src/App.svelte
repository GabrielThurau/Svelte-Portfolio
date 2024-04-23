<script>
  import Button from "./lib/Button.svelte";
  import Container from "./lib/Container.svelte";
  import FaAngleLeft from "svelte-icons/fa/FaAngleLeft.svelte";
</script>

<Container>
  <Button let:x={z} size="large" shadow bgColor="salmon" txtColor="white">
    <div style:width="20px" slot="leftText"><FaAngleLeft /></div>
    Button Text {z}
  </Button>
  <h1 slot="header">This is a header for the section</h1>
  <p slot="content">This is content for the section</p>
</Container>
