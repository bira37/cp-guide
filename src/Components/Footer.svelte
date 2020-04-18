<script>
  import DiGithubBadge from "svelte-icons/di/DiGithubBadge.svelte";
  import IoLogoLinkedin from "svelte-icons/io/IoLogoLinkedin.svelte";
  import IoMdMail from "svelte-icons/io/IoMdMail.svelte";
  import MdPerson from "svelte-icons/md/MdPerson.svelte";
</script>

<style type="text/scss">
  @import "../Styles/variables.scss";

  .footer {
    background-color: $footerBackground;
    color: white;
    position: fixed;
    bottom: 0;
    width: 100vw;
  }

  .info {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }

  .info-item {
    margin: 1rem;
    width: 2rem;
    height: 2rem;
    text-align: center;
    color: white;
  }

  .made-by {
    text-align: center;
    padding-bottom: 0.5rem;
  }
</style>

<div class="footer">
  <div class="info">
    <a
      class="info-item"
      href="https://github.com/bira37/"
      target="_blank"
      title="GitHub">
      <DiGithubBadge />
    </a>
    <a
      class="info-item"
      href="https://www.linkedin.com/in/bira37/?locale=en_US"
      target="_blank"
      title="LinkedIn">
      <IoLogoLinkedin />
    </a>
    <a
      class="info-item"
      href="mailto:ubiratanneto37@gmail.com"
      target="_blank"
      title="E-mail">
      <IoMdMail />
    </a>
    <a
      class="info-item"
      href="https://bira37.github.io/"
      target="_blank"
      title="Personal Website">
      <MdPerson />
    </a>
  </div>
  <div class="made-by">Created by Ubiratan Neto</div>
</div>
