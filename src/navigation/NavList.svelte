<script>
  import { createEventDispatcher } from "svelte";
  import { navList } from "./PagesList.svelte";

  export let active;

  const dispatch = createEventDispatcher();
</script>

<div class:active>
  <ul class="navbar-list" on:click>
    {#each navList as item}
      <li
        class="item"
        on:click={() => {
          dispatch(item.name);
        }}
        title={item.title}
      >
        {@html item.icon}
      </li>
    {/each}
  </ul>
</div>

<style lang="scss">
  div :global(li svg) {
    fill: var(--just-white);
    width: 21px;
  }

  :global(body.darkmode) {
    .navbar-list .item {
      background-color: var(--almost-black);
    }
  }

  div {
    align-items: center;
    box-sizing: border-box;
    display: flex;
    transition: transform var(--transition-time);
    z-index: 2;

    &.active {
      .navbar-list .item {
        &:first-of-type {
          transform: translateX(165px);
        }
        &:nth-of-type(2) {
          transform: translateX(178px);
        }
        &:nth-of-type(3) {
          transform: translateX(181px);
        }
        &:nth-of-type(4) {
          transform: translateX(178px);
        }
        &:last-of-type {
          transform: translateX(165px);
        }
      }
    }
  }

  .navbar-list {
    box-sizing: border-box;
    left: calc(-1 * var(--navigation-width));
    list-style: none;
    padding-left: 0;
    position: fixed;
    top: 50%;
    transform: translateY(-50%);
    width: var(--navigation-width);
    z-index: 2;

    .item {
      align-items: center;
      background-color: var(--maastricht-blue);
      border-radius: 50%;
      border: 2px solid transparent;
      box-sizing: border-box;
      color: var(--just-white);
      cursor: pointer;
      display: flex;
      font-size: 1.2rem;
      height: 55px;
      justify-content: center;
      margin-bottom: 13px;
      margin-top: 13px;
      transition: border-color var(--transition-time),
        transform var(--transition-time);
      width: 55px;

      &:hover {
        border-color: var(--pegasus-red);
      }

      &:first-of-type {
        transform: translateX(-89px);
      }
      &:nth-of-type(2) {
        transform: translateX(-144px);
      }
      &:nth-of-type(3) {
        transform: translateX(-233px);
      }
      &:nth-of-type(4) {
        transform: translateX(-377px);
      }
      &:last-of-type {
        transform: translateX(-610px);
      }
    }
  }
</style>
