<script>
  import { onMount } from "svelte";
  import { changeMode } from "./darkmode/Darkmode.svelte";
  import AboutPage from "./pages/about/About.svelte";
  import ContactPage from "./pages/contact/Contact.svelte";
  import ExperiencePage from "./pages/experience/Experience.svelte";
  import Navigation from "./navigation/Navigation.svelte";
  import SkillsPage from "./pages/skills/Skills.svelte";
  import StartPage from "./pages/start/Start.svelte";

  let renderComponent = StartPage;
  let isDarkmode = false;

  const listenModeChange = () => {
    window.matchMedia("(prefers-color-scheme: light)").addListener(() => {
      changeMode();
      isDarkmode = !isDarkmode;
    });
  };

  onMount(() => {
    if (
      window.matchMedia &&
      window.matchMedia("(prefers-color-scheme: dark)").matches
    ) {
      changeMode();
      listenModeChange();
      isDarkmode = !isDarkmode;
    } else {
      listenModeChange();
    }
  });
</script>

<section>
  <Navigation
    on:AboutPage={() => {
      renderComponent = AboutPage;
    }}
    on:StartPage={() => {
      renderComponent = StartPage;
    }}
    on:SkillsPage={() => {
      renderComponent = SkillsPage;
    }}
    on:ExperiencePage={() => {
      renderComponent = ExperiencePage;
    }}
    on:ContactPage={() => {
      renderComponent = ContactPage;
    }}
    {isDarkmode}
  />
</section>

<section class="content">
  <svelte:component this={renderComponent} />
</section>

<style lang="scss">
  .content {
    box-sizing: border-box;
    margin-left: var(--navigation-width);
    min-height: 100vh;
    padding-bottom: 21px;
    padding-top: 21px;
    width: 100%;
  }
</style>
