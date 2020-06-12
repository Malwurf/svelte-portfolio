<script>
  import PageHeadline from "../../pageheadline/PageHeadline.svelte";
  import { jobsList } from "./JobsList.svelte";

  function opinionLink(name) {
    let link = "opinions/" + name.toLowerCase().replace(/[\s\.]/g, "") + ".pdf";
    return link;
  }

  const headline = "Experience timeline";
</script>

<style lang="scss">
  :global(body.darkmode) {
    .jobs-list {
      .item {
        background-color: var(--almost-black);

        .content {
          border-color: var(--just-white);

          &:before {
            @media all and (min-width: 768px) {
              border-left-color: var(--just-white);
            }
          }

          .opinion {
            &:hover {
              color: var(--just-blue);
            }
          }
        }

        &:nth-of-type(even) {
          .content:before {
            @media all and (min-width: 768px) {
              border-right-color: var(--just-white);
            }
          }
        }
      }
    }
  }

  .jobs-list {
    align-items: center;
    display: flex;
    flex-direction: column;
    list-style: none;
    margin-bottom: 55px;
    margin-top: 55px;
    padding-left: 0;
    position: relative;

    @media all and (min-width: 768px) {
      align-items: flex-start;
    }

    @media all and (min-width: 768px) {
      &:before {
        color: var(--pegasus-red);
        content: "Future";
        left: 50%;
        position: absolute;
        top: -30px;
        transform: translateX(-50%);
      }

      &:after {
        background-color: var(--pegasus-red);
        bottom: 0;
        content: "";
        left: 50%;
        margin-top: -13px;
        position: absolute;
        top: 0;
        transform: translateX(-50%);
        width: 3px;
      }
    }

    .item {
      margin-bottom: 0px;
      position: relative;
      width: 100%;

      & + .item {
        margin-top: 34px;

        @media all and (min-width: 768px) {
          margin-top: 0;
        }
      }

      @media all and (min-width: 768px) {
        width: 50%;
      }

      .content {
        border: 2px solid var(--maastricht-blue);
        box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
        box-sizing: border-box;
        max-width: 1270px;
        padding: 21px;
        position: relative;
        transition: box-shadow var(--transition-time);
        width: 100%;

        @media all and (min-width: 768px) {
          width: calc(100% - 25px);

          &:hover {
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16),
              0 3px 6px rgba(0, 0, 0, 0.23);
          }
        }

        &:before {
          border-width: 0 13px 13px 13px;
          border-color: transparent transparent var(--pegasus-red) transparent;
          left: 50%;
          transform: translateX(-50%);
          top: -13px;
          border-style: solid;
          content: " ";
          display: block;
          height: 0;
          position: absolute;
          width: 0;

          @media all and (min-width: 768px) {
            border-color: transparent transparent transparent
              var(--maastricht-blue);
            border-width: 13px 0 13px 13px;
            right: -13px;
            top: 34px;
            transform: none;
            left: auto;
          }
        }

        .headline {
          color: var(--just-blue);
          margin: 0;
        }

        p {
          margin-top: 13px;
          margin-bottom: 13px;
        }

        .description {
          .job-title {
            margin-top: 3px;
          }

          .job-description {
            font-size: 18px;
          }
        }

        .opinion {
          color: var(--pegasus-red);
          display: inline-block;
          margin-top: 13px;
          text-decoration: none;
          transition: color var(--transition-time);
          font-size: 18px;
          font-weight: bolder;

          @media (hover: hover) and (pointer: fine) and (min-width: 768px) {
            &:hover {
              color: var(--maastricht-blue);
            }
          }
        }

        .date {
          font-size: 14px;
          font-weight: bolder;
          margin-top: 5px;
        }

        .clients {
          font-style: italic;
        }
      }

      &:nth-of-type(even) {
        align-self: center;
        display: flex;
        justify-content: flex-end;

        @media all and (min-width: 768px) {
          align-self: flex-end;
        }

        .content {
          &:before {
            border-color: transparent transparent var(--pegasus-red) transparent;
            border-width: 0 13px 13px 13px;
            left: 50%;
            top: -13px;
            transform: translateX(-50%);

            @media all and (min-width: 768px) {
              border-color: transparent var(--maastricht-blue) transparent
                transparent;
              border-width: 13px 13px 13px 0;
              left: -13px;
              top: 34px;
              transform: none;
            }
          }
        }
      }
    }
  }
</style>

<PageHeadline {headline} />

<div class="container">
  <ul class="jobs-list">
    {#each jobsList as job}
      <li class="item target">
        <div class="content">
          <h2 class="headline">{job.name}</h2>
          <div class="description">
            <div class="job-title">{job.title}</div>
            <p class="date">{job.startDate} - {job.endDate}</p>
            <p class="job-description">{job.description}</p>
            <p class="clients">Clients - {job.clients.join(', ')}</p>
            <p>{job.technologies.join(', ')}</p>
          </div>
          {#if job.opinion}
            <a href={opinionLink(job.name)} target="_blank" class="opinion">
              See opinion
            </a>
          {/if}
        </div>
      </li>
    {/each}
  </ul>
</div>
