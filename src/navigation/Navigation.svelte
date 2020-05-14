<script>
  import NavList from "./NavList.svelte";
  import NavTrigger from "./NavTrigger.svelte";

  let active = false;
  let ChoosenPage = "StartPage";

  function handleTrigger() {
    active = !active;
  }
</script>

<style>
  nav {
    display: flex;
  }
</style>

<nav>
  <NavTrigger on:change={handleTrigger} isChecked={active} />
  <NavList
    {active}
    on:AboutPage
    on:StartPage
    on:PortfolioPage
    on:ContactPage
    on:click={handleTrigger} />
</nav>
