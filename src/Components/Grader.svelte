<script>
  export let grade;
  import IoIosStar from "svelte-icons/io/IoIosStar.svelte";
  import IoIosStarOutline from "svelte-icons/io/IoIosStarOutline.svelte";
  const full_stars = [];
  const empty_stars = [];
  for (let i = 1; i <= grade; i++) {
    full_stars.push(1);
  }
  for (let i = grade + 1; i <= 5; i++) {
    empty_stars.push(1);
  }
</script>

<style type="text/scss">
  @import "../Styles/variables.scss";
  .icon {
    height: 1rem;
    width: 1rem;
    margin-top: ($defaultMargin + 0.5rem)/2;
    &:first-child {
      margin-left: $defaultMargin/2;
    }
  }

  .grade {
    display: flex;
    flex-wrap: nowrap;
  }
</style>

<span class="grade">
  {#each full_stars as star}
    <div class="icon">
      <IoIosStar />
    </div>
  {/each}
  {#each empty_stars as star}
    <div class="icon">
      <IoIosStarOutline />
    </div>
  {/each}
</span>
