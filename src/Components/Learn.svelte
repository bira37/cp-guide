<script>
  import data from "../learnData.json";
  import LearnCategory from "./LearnCategory.svelte";
  for (let i = 0; i < data.length; i++) {
    data[i].topics.sort((a, b) => {
      return a.difficulty <= b.difficulty ? -1 : 1;
    });
  }
</script>

<style type="text/scss">
  @import "../Styles/shared.scss";

  .categories {
    display: flex;
    flex-direction: column;
    list-style-type: none;
    margin-left: $defaultMargin;
    margin-right: $defaultMargin;
    padding: 0;
  }

  .category {
    color: $primaryColor;
    margin: 0;
    padding: 0.5rem;
    display: inline;
    flex: 0 1 auto;

    &:nth-child(2n + 1) {
      background-color: $ternaryColor;
      transition: background-color 200ms ease-in;
    }

    &:nth-child(2n + 1):hover {
      background-color: lighten($ternaryColor, 5%);
    }

    &:nth-child(2n) {
      background-color: #3c6e71;
      transition: background-color 200ms ease-in;
    }

    &:nth-child(2n):hover {
      background-color: lighten(#3c6e71, 5%);
    }
  }
</style>

<div class="wrapper">
  <div class="subtitle">
    <h2>Learn</h2>
    <p>Choose a category below to show the topics:</p>
  </div>
  <ul class="categories">
    {#each data as category}
      <li class="category">
        <LearnCategory {category} />
      </li>
    {/each}
  </ul>
</div>
