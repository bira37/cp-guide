<script>
  import { path } from "../stores";
</script>

<style type="text/scss">
  @import "../Styles/variables.scss";

  .title {
    font-size: 2.5rem;
    color: $secondaryColor;
    margin-left: $defaultMargin;
  }

  .navbar {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    border-top: 1px solid $ternaryColor;
    padding-top: 1rem;
  }

  .nav-item {
    color: $secondaryColor;
    font-size: 1.25rem;
    margin: 0 $defaultMargin;
    transition: color 300ms ease;
    &:hover {
      color: $quaternaryColor;
      cursor: pointer;
    }
  }
</style>

<h1 class="title">Competitive Programming Guide</h1>

<nav class="navbar">
  <span class="nav-item" on:click={() => path.set('home')}>Home</span>
  <span class="nav-item" on:click={() => path.set('learn')}>Learn</span>
  <span class="nav-item" on:click={() => path.set('extra')}>
    Where to Practice
  </span>
</nav>
