<script>
  import NavList from "./NavList.svelte";
  import NavTrigger from "./NavTrigger.svelte";
  import DarkmodeTrigger from "./DarkmodeTrigger.svelte";

  export let isDarkmode;

  let active = false;

  const handleTrigger = () => {
    active = !active;
  };
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
  <DarkmodeTrigger {isDarkmode} />
</nav>

<style>
  :global(body.darkmode nav) {
    background-color: var(--almost-black);
  }

  nav {
    align-items: center;
    background-color: var(--maastricht-blue);
    bottom: 0;
    box-shadow: 3px 0 5px rgba(0, 0, 0, 0.21);
    display: flex;
    justify-content: center;
    left: 0;
    position: fixed;
    top: 0;
    width: var(--navigation-width);
    z-index: 3;
    flex-direction: column;
  }
</style>
