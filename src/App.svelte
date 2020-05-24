<script>
  import AboutPage from "./pages/about/About.svelte";
  import ContactPage from "./pages/contact/Contact.svelte";
  import ExperiencePage from "./pages/experience/Experience.svelte";
  import Navigation from "./navigation/Navigation.svelte";
  import SkillsPage from "./pages/skills/Skills.svelte";
  import StartPage from "./pages/start/Start.svelte";

  let renderComponent = StartPage;
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
  />
</section>

<section class="content">
  <svelte:component this={renderComponent} />
</section>
