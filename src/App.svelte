<script>
  import AboutPage from "./pages/about/About.svelte";
  import ContactPage from "./pages/contact/Contact.svelte";
  import CvPage from "./pages/cv/cv.svelte";
  import Navigation from "./navigation/Navigation.svelte";
  import PortfolioPage from "./pages/portfolio/Portfolio.svelte";
  import StartPage from "./pages/start/Start.svelte";

  let renderComponent = StartPage;
</script>

<style lang="scss">
  .content {
    margin-left: 30px;
  }
</style>

<section>
  <Navigation
    on:AboutPage={() => {
      renderComponent = AboutPage;
    }}
    on:StartPage={() => {
      renderComponent = StartPage;
    }}
    on:CvPage={() => {
      renderComponent = CvPage;
    }}
    on:PortfolioPage={() => {
      renderComponent = PortfolioPage;
    }}
    on:ContactPage={() => {
      renderComponent = ContactPage;
    }} />
</section>

<section class="content">
  <svelte:component this={renderComponent} />
</section>
