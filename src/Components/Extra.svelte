<script>

</script>

<style type="text/scss">
  @import "../Styles/shared.scss";

  ul {
    list-style-type: square;
    margin-left: $defaultMargin;
    margin-right: $defaultMargin;
  }
  ul li {
    font-size: 1.25rem;
    color: $secondaryColor;
    padding-top: 1rem;
    &:first-child {
      padding-top: 0.5rem;
    }
  }
  a {
    font-size: 1.25rem;
    color: $ternaryColor;
    transition: color 300ms ease-in;
    &:hover {
      color: $quaternaryColor;
    }
  }

  .additional {
    margin-top: 1.5 * $defaultMargin;
    margin-left: $defaultMargin;
    color: $secondaryColor;

    font-size: 1.25rem;
  }
</style>

<div class="wrapper">
  <div class="subtitle">
    <h2>Where to Practice</h2>
    <p>
      Here are listed some well known and good platforms where you can start
      practicing. While you continue training, you will discover even more
      platforms with different problems
    </p>
  </div>
  <ul>
    <li>
      <a href="https://cses.fi/problemset/list/" target="_blank">
        CSES - Code Submission Evaluation System
      </a>
      : This website contains some classic problems with short statements,
      divided by categories. Great for practicing new learned techniques and
      algorithms.
    </li>
    <li>
      <a href="https://www.urionlinejudge.com.br/" target="_blank">
        URI Online Judge
      </a>
      : This one contains classic problems, but also contains a beginner
      section. The problems are divided by categories and difficulty levels. The
      overall design is more user friendly, and can be the better option for who
      is still in the beginning.
    </li>
    <li>
      <a href="https://codeforces.com" target="_blank">Codeforces</a>
      : This website hosts more than one online competitions every week. There
      you can find an active community, problems from old competitions, divided
      by categories and difficulty level, and a blog where people are constantly
      helping others and sharing new algorithms and knowledge.
    </li>
    <li>
      <a href="https://spoj.com" target="_blank">SPOJ</a>
      : Despite being old, this well known website has a bunch of classic
      problems and still a good option to practice.
    </li>
  </ul>
  <p class="additional">
    Also, if you are stuck in a problem and wants to see the solution, check out
    <a href="https://github.com/bira37/problem-solutions">this repository.</a>
    Here you can find the solution for more than 1000 problems from my own
    training sessions and from other contributors. It is regularly updated with
    new solutions. It is open for contribution, to make it bigger and offer
    solutions to even more problems.
  </p>
</div>
