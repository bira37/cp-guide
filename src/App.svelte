<script>
  import Nav from "./Components/Nav.svelte";
  import Content from "./Components/Content.svelte";
  import Footer from "./Components/Footer.svelte";
</script>

<style type="text/scss">
  @import "./Styles/variables.scss";
  :global(body) {
    background-color: $primaryColor;
    height: 100%;
    margin: 0px;
    padding: 0px;
  }

  :global(html) {
    height: 100%;
    font-size: 16px;
  }

  :global(*),
  :global(*:before),
  :global(*:after) {
    box-sizing: inherit;
  }
</style>

<Nav />
<Content />
<Footer />
