<script>
  import PageHeadline from "../../pageheadline/PageHeadline.svelte";
  import { skillsList } from "./SkillsList.svelte";

  const headline = "My skills";
</script>

<PageHeadline {headline} />

<div class="container">
  <ul class="skillsList">
    {#each skillsList as skill}
      <li class="{skill.category == 'spacer' ? 'spacer' : 'target'} item">
        <span class="symbol">{skill.symbol}</span>
        <span class="name">{skill.name}</span>
        <span class="description">
          [{skill.category}] - {skill.description}
        </span>
      </li>
    {/each}
  </ul>
</div>

<style lang="scss">
  :global(body.darkmode) {
    .skillsList {
      .item {
        border-color: var(--just-white);
      }
    }
  }

  .skillsList {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    max-width: 987px;
    padding-left: 0;

    @media (hover: hover) and (pointer: fine) and (min-width: 1024px) {
      display: grid;
      grid-column-gap: 8px;
      grid-row-gap: 13px;
      grid-template-columns: repeat(8, 89px);
      margin: auto;
    }

    .item {
      border: 2px solid var(--maastricht-blue);
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
      box-sizing: border-box;
      display: flex;
      flex-direction: column;
      justify-content: center;
      margin-bottom: 21px;
      margin-left: 8px;
      margin-right: 8px;
      min-width: 100%;
      padding: 8px;
      position: relative;
      width: calc(50% - 16px);

      @media all and (min-width: 520px) {
        min-width: auto;
      }

      @media (hover: hover) and (pointer: fine) and (min-width: 1024px) {
        height: 89px;
        margin: 0;
        min-width: auto;
        transition: color var(--transition-time),
          border-color var(--transition-time),
          background-color var(--transition-time);
        width: 89px;

        &:hover {
          &:not(.spacer) {
            background-color: var(--pegasus-red);
            border-color: var(--pegasus-red);
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16),
              0 3px 6px rgba(0, 0, 0, 0.23);
            color: var(--just-white);

            .description {
              display: block;
            }
          }
        }
      }

      &.spacer {
        display: none;

        @media (hover: hover) and (pointer: fine) and (min-width: 1024px) {
          border: none;
          box-shadow: none;
          display: block;
        }
      }

      .symbol {
        font-size: 34px;
      }

      .name {
        font-size: 13px;
      }

      .description {
        border-radius: 5px;
        font-size: 13px;
        margin-top: 13px;

        @media (hover: hover) and (pointer: fine) and (min-width: 1024px) {
          background-color: var(--maastricht-blue);
          color: var(--just-white);
          display: none;
          left: 50%;
          margin-top: 0;
          padding: 5px 8px;
          position: absolute;
          top: calc(100% + 0px);
          transform: translateX(-50%);
          width: 233px;
          z-index: 1;
        }
      }
    }
  }
</style>
