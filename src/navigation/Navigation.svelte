<style>
  nav {
    display: flex;
  }
</style>

<script>
  import NavList from "./NavList.svelte";
  import NavTrigger from "./NavTrigger.svelte";

  let active = false;
  let ChoosenPage = "StartPage";

  function handleTrigger() {
    active = !active;
  }
</script>

<nav>
  <NavTrigger on:change={handleTrigger} isChecked={active} />
  <NavList
    {active}
    on:AboutPage
    on:ContactPage
    on:ExperiencePage
    on:SkillsPage
    on:StartPage
    on:click={handleTrigger}
  />
</nav>
