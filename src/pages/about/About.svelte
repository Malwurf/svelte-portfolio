<script>
  import PageHeadline from "../../pageheadline/PageHeadline.svelte";
  import { aboutMe } from "./AboutDesc.svelte";

  const cite = '"Love You 3000"';
  const headline = "About me in a pill";
  const name = "Przemysław Korościk";
  const title = "Frontend Developer";
</script>

<PageHeadline {headline} />

<div class="container">
  <h2 class="blue headline target">{title}</h2>
  <h1 class="main headline">{name}</h1>

  <ul class="about-list">
    {#each aboutMe as item}
      <li class="item target">
        <span class="icon">
          {@html item.icon}
        </span>
        <p class="text">{item.description}</p>
      </li>
    {/each}
  </ul>

  <h2 class="red headline quotation">{cite}</h2>
</div>

<style lang="scss">
  .about-list {
    align-items: center;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: space-between;
    list-style: none;
    max-width: 987px;
    padding-left: 0;

    @media screen and (min-width: 1024px) {
      flex-direction: row;
    }

    .item {
      align-items: center;
      display: flex;
      justify-content: flex-start;
      margin-bottom: 21px;
      width: 89%;

      @media screen and (min-width: 1024px) {
        width: 50%;
      }
    }

    .text {
      font-size: 13px;

      @media screen and (min-width: 640px) {
        font-size: 21px;
      }
    }

    .icon {
      border-right: 2px solid var(--pegasus-red);
      display: block;
      height: 100%;
      margin-right: 20px;
      max-height: 34px;
      max-width: 34px;
      padding-bottom: 8px;
      padding-right: 13px;
      padding-top: 8px;
      position: relative;
      width: 100%;

      @media screen and (min-width: 640px) {
        max-height: 55px;
        max-width: 55px;
        padding: 13px 21px;
      }
    }
  }

  .headline {
    &.red {
      color: var(--pegasus-red);
      margin: 0;
    }

    &.blue {
      color: var(--just-blue);
      font-size: 13px;
      margin-bottom: 13px;
      margin-top: 0;

      @media screen and (min-width: 640px) {
        font-size: 21px;
      }
    }

    &.quotation {
      font-size: 21px;
      font-style: italic;
      font-weight: lighter;
    }

    &.main {
      font-size: 21px;
      margin: 0;

      @media screen and (min-width: 640px) {
        font-size: 34px;
      }
    }
  }
</style>
