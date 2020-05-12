<script>
  import { createEventDispatcher } from "svelte";

  export let opened;

  const dispatch = createEventDispatcher();
</script>

<style lang="scss">
  section {
    align-items: flex-start;
    background-color: var(--feather-blue);
    box-sizing: border-box;
    display: flex;
    height: 100vh;
    justify-content: center;
    overflow-y: scroll;
    position: absolute;
    transform: translateX(-380px);
    transition: transform var(--transition-time);
    width: 300px;
    z-index: 2;

    &.opened {
      transform: translateX(0);
    }
  }
  ul {
    list-style: none;
    padding: 30px 0 30px;
    width: 100%;
    box-sizing: border-box;
    margin: 0;

    li {
      align-items: center;
      color: var(--bleachedsilk-white);
      cursor: pointer;
      display: flex;
      font-size: 1.2rem;
      height: 100px;
      justify-content: center;

      & + li,
      &:first-of-type {
        border-top: 2px solid red;
      }

      &:last-of-type {
        border-bottom: 2px solid red;
      }
    }
  }
</style>

<section class:opened>
  <ul class="navbar-list" on:click>
    <li
      class="item"
      on:click={() => {
        dispatch('StartPage');
      }}>
      Start
    </li>
    <li
      class="item"
      on:click={() => {
        dispatch('AboutPage');
      }}>
      About
    </li>
    <li
      class="item"
      on:click={() => {
        dispatch('CvPage');
      }}>
      CV
    </li>
    <li
      class="item"
      on:click={() => {
        dispatch('PortfolioPage');
      }}>
      Portfolio
    </li>
    <li
      class="item"
      on:click={() => {
        dispatch('ContactPage');
      }}>
      Contact
    </li>
  </ul>
</section>
