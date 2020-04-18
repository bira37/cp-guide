<script>
  export let category;
  import FaCaretDown from "svelte-icons/fa/FaCaretDown.svelte";
  import FaCaretUp from "svelte-icons/fa/FaCaretUp.svelte";
  import Grader from "./Grader.svelte";
  $: isActive = false;

  function toggleCategory() {
    isActive = !isActive;
  }
</script>

<style type="text/scss">
  @import "../Styles/variables.scss";

  .title {
    display: flex;
    justify-content: space-between;

    &:hover {
      cursor: pointer;
    }
  }
  .caret {
    margin-top: 0.5rem;
    height: 2rem;
    width: 2rem;
  }

  .content {
    @include fade-animation;

    .topic {
      margin-bottom: 0.5rem;

      ul li {
        margin-top: 0.5rem;
        &:first-child {
          margin-top: 0;
        }
      }
      ul li a {
        text-decoration: underline;
        color: $primaryColor;
        transition: color 300ms ease;
        &:hover {
          color: $quaternaryColor;
        }
      }
    }
  }
</style>

<div class="title" on:click={() => toggleCategory()}>
  <p>{category.name}</p>
  {#if isActive}
    <div class="caret">
      <FaCaretUp />
    </div>
  {:else}
    <div class="caret">
      <FaCaretDown />
    </div>
  {/if}
</div>

{#if isActive}
  <div class="content">
    <ul>
      {#each category.topics as topic}
        <li class="topic">
          <div class="topic-info">
            <p>
              {topic.title}
              <Grader grade={topic.difficulty} />
            </p>
          </div>
          <ul>
            {#each topic.links as link}
              <li>
                <a href={link.url} target="_blank">{link.site}</a>
              </li>
            {/each}
          </ul>
        </li>
      {/each}
    </ul>
  </div>
{/if}
