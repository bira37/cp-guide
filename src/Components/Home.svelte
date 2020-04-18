<script>
  import { path } from "../stores";
</script>

<style type="text/scss">
  @import "../Styles/variables.scss";

  .choice {
    @include fade-animation;
    display: flex;
    flex-direction: row;
    align-items: stretch;
    padding-top: 2rem;
    margin-bottom: 8rem;
  }

  .choice1 {
    color: $primaryColor;
    background-color: #3c6e71;

    a {
      color: $primaryColor;
      text-decoration: underline;
      transition: color 300ms ease;
      display: block;
      padding-bottom: 1rem;
      &:hover {
        color: $quaternaryColor;
      }
    }
  }
  .choice1 {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    flex-wrap: wrap;
    h2,
    p,
    a {
      margin-left: $defaultMargin;
      align-self: flex-start;
    }

    p a {
      display: inline;
      margin: 0;
      padding: 0;
    }
  }
</style>

<div class="choice">
  <div class="choice1">
    <div>
      <h2>Find where to learn here</h2>
      <p>
        Here you will find a large list of great tutorials and topics that will
        present you new algorithms and data structures, improving your overall
        logical and coding skills. These resources are well known by the
        majority of competitors, and include websites like Codeforces,
        CP-Algorithms, TopCoder, Hackerearth, Brilliant, Geeks for Geeks and
        others. This guide is open to contribution via it's
        <a href="https://github.com/bira37/cp-guide">GitHub repository.</a>

      </p>
    </div>
    <a href="javascript:void(0)" on:click={() => path.set('learn')}>
      Click here to go to the Learn Page
    </a>
  </div>
</div>
