<script>
  import NavList from './NavList.svelte';
  import NavTrigger from './NavTrigger.svelte';

  let opened = false;

  function handleTrigger() {
    opened = !opened;
  };
</script>

<style>
nav {
  display: flex;
}
</style>

<nav>
  <NavTrigger on:change={handleTrigger}/>
  <NavList opened={opened}/>
</nav>
