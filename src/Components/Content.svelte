<script>
  import { path } from "../stores";
  import Home from "./Home.svelte";
  import Learn from "./Learn.svelte";
  import Extra from "./Extra.svelte";

  let path_val;

  const unsubscribe = path.subscribe(val => {
    path_val = val;
  });
</script>

<style type="text/scss">

</style>

{#if path_val === 'home'}
  <Home />
{:else if path_val === 'learn'}
  <Learn />
{:else if path_val === 'extra'}
  <Extra />
{/if}
