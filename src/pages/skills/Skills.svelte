<script>
  const skillsList = [
    {
      symbol: "JS",
      name: "JavaScript",
      description:
        "I'm not a JS ninja, but I'm familiar with ES6 syntax and know the difference between ECMAScript and JavaScript.",
      category: "Skill"
    },
    {
      symbol: "SE",
      name: "Svelte",
      description:
        "Great JavaScript transpiler. I love that syntax, this page was written in Svelte.",
      category: "Skill"
    },
    {
      symbol: "",
      name: "",
      description: "",
      category: "spacer"
    },
    {
      symbol: "",
      name: "",
      description: "",
      category: "spacer"
    },
    {
      symbol: "",
      name: "",
      description: "",
      category: "spacer"
    },
    {
      symbol: "HL",
      name: "HTML",
      description: "I know HTML 5 syntax and I write semantic code.",
      category: "Skill"
    },
    {
      symbol: "SS",
      name: "SASS",
      description: "I love SASS. It should replace plain CSS.",
      category: "Skill"
    },
    {
      symbol: "LS",
      name: "Less",
      description: "I like SASS instead less but I know both syntaxes.",
      category: "Skill"
    },
    {
      symbol: "CS",
      name: "CSS",
      description: "I know HTML syntax and I write semantic code.",
      category: "Skill"
    },
    {
      symbol: "JQ",
      name: "jQuery",
      description:
        "I've worked using that library a lot but now we have better solutions e.g. Svelte / React or Vanilla JS.",
      category: "Skill"
    },
    {
      symbol: "BP",
      name: "Bootstrap",
      description:
        "I know very well this CSS framework but I prefer to write my own styles to projects if I can.",
      category: "Skill"
    },
    {
      symbol: "PA",
      name: "PWA",
      description:
        "I know the core assumption of PWA. I can implement a default functionalities e.g. offline first.",
      category: "Skill"
    },
    {
      symbol: "RD",
      name: "RWD",
      description:
        "I use the Responsive Web Design concept every day. Mobile users are most important!",
      category: "Skill"
    },
    {
      symbol: "FX",
      name: "Flexbox",
      description: "Flexbox concept is my best friend!",
      category: "Skill"
    },
    {
      symbol: "MO",
      name: "Magento",
      description:
        "I had the Magento project for about one year but I don't like that eCommerce system.",
      category: "Skill"
    },
    {
      symbol: "GT",
      name: "Git",
      description: "In case of fire, git commit, git push and leave bulding!",
      category: "Skill"
    },
    {
      symbol: "PS",
      name: "Photoshop",
      description:
        "I'm NOT a Graphic Designer but I feel fluent in cutting graphics for websites.",
      category: "Tool"
    },
    {
      symbol: "AI",
      name: "Illustrator",
      description: "Same as Photoshop but in Illustrator :)",
      category: "Tool"
    },
    {
      symbol: "MO",
      name: "MacOS",
      description:
        "I'm experienced in the Apple ecosystem and I love to work on Macs. MacOS combines Linux stability and Windows UX.",
      category: "Tool"
    },
    {
      symbol: "JI",
      name: "JIRA",
      description:
        "I have 2+ years of experience working on Jira but I'm not experienced like Project Manager.",
      category: "Tool"
    },
    {
      symbol: "SL",
      name: "Slack",
      description: "Great to be here :)",
      category: "Tool"
    },
    {
      symbol: "TL",
      name: "Trello",
      description:
        "Everyone knows that is the best task manager! Simply and easy to use.",
      category: "Tool"
    },
    {
      symbol: "SH",
      name: "Sketch",
      description:
        "I know how to cut icons and graphics from mockups and use it on a web page.",
      category: "Tool"
    },
    {
      symbol: "FI",
      name: "Figma",
      description: "Figma is online version of Sketch ;)",
      category: "Tool"
    },
    {
      symbol: "",
      name: "",
      description: "",
      category: "spacer"
    },
    {
      symbol: "EL",
      name: "Email",
      description:
        "I don't like it, but I have experience with making email templates.",
      category: "Skill"
    },
    {
      symbol: "NP",
      name: "NPM",
      description:
        "IMO there is no big difference to use NPM or Yarn in a project but no both!",
      category: "Tool"
    },
    {
      symbol: "GP",
      name: "Gulp",
      description:
        "I know how to add gulp to existing projects and automate some tasks making gulp pipes.",
      category: "Skill"
    },
    {
      symbol: "AE",
      name: "After Effects",
      description:
        "A long time ago in a galaxy... Yes, I did a couple of movies with special effects. I'm a bit ashamed of the effect but it was my studies project.",
      category: "Tool"
    },
    {
      symbol: "MO",
      name: "Microsoft Office",
      description:
        "I know default Office programs, Excel, Word, PowerPoint, but nope, I will not write a game in excel using VBA... maybe using StackOverflow ;)",
      category: "Tool"
    },
    {
      symbol: "",
      name: "",
      description: "",
      category: "spacer"
    },
    {
      symbol: "",
      name: "",
      description: "",
      category: "spacer"
    },
    {
      symbol: "",
      name: "",
      description: "",
      category: "spacer"
    },
    {
      symbol: "",
      name: "",
      description: "",
      category: "spacer"
    },
    {
      symbol: "GD",
      name: "Good Organised",
      description:
        "IMO good work organization is required when you work remotely.",
      category: "Soft"
    },
    {
      symbol: "CH",
      name: "Chatty",
      description:
        "I'm communicative person, but not when I'm fresh in the team :) I tell honestly about my project/team and tasks estimation exceeded.",
      category: "Soft"
    },
    {
      symbol: "RW",
      name: "Remote Work",
      description:
        "I'm a remote worker from the half of 2019. I feel good with that.",
      category: "Soft"
    }
  ];
</script>

<style lang="scss">
  .skillsList {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    max-width: 987px;
    padding-left: 0;

    @media all and (min-width: 1024px) {
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
      min-width: 100%;
      padding: 8px;
      position: relative;
      width: calc(50% - 32px);

      @media all and (min-width: 520px) {
        min-width: auto;
        width: calc(50% - 32px);
      }

      @media all and (min-width: 1024px) {
        height: 89px;
        min-width: auto;
        transition: color var(--transition-time),
          border-color var(--transition-time),
          background-color var(--transition-time);
        width: 89px;

        &:hover {
          &:not(.spacer) {
            background-color: var(--persian-red);
            border-color: var(--persian-red);
            box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16),
              0 3px 6px rgba(0, 0, 0, 0.23);
            color: var(--white);

            .description {
              display: block;
            }
          }
        }
      }

      &.spacer {
        display: none;

        @media all and (min-width: 1024px) {
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

        @media all and (min-width: 1024px) {
          background-color: var(--maastricht-blue);
          color: var(--white);
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

<div class="container">
  <ul class="skillsList">
    {#each skillsList as skill}
      <li class="{skill.category} item">
        <span class="symbol">{skill.symbol}</span>
        <span class="name">{skill.name}</span>
        <span class="description">
          [{skill.category}] - {skill.description}
        </span>
      </li>
    {/each}
  </ul>
</div>
