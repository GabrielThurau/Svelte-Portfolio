<script>
  import Button from "./lib/Button.svelte";
  import Container from "./lib/Container.svelte";
</script>

<Button size="large"></Button>
<Container>
  <h1 slot="header">This is a header for the section</h1>
  <p slot="content">This is content for the section</p>
</Container>
