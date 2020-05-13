<script>
  import NavList from "./NavList.svelte";
  import NavTrigger from "./NavTrigger.svelte";

  let opened = false;
  let ChoosenPage = "StartPage";

  function handleTrigger() {
    opened = !opened;
  }
</script>

<style>
  nav {
    display: flex;
  }
</style>

<nav>
  <NavTrigger on:change={handleTrigger} isChecked={opened} />
  <NavList
    {opened}
    on:AboutPage
    on:StartPage
    on:PortfolioPage
    on:ContactPage
    on:click={handleTrigger} />
</nav>
