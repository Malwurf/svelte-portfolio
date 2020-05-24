<script>
  const skillsList = [
    {
      symbol: "JS",
      name: "JavaScript",
      description: "desc here",
      category: "soft"
    },
    {
      symbol: "SE",
      name: "Svelte",
      description: "desc here",
      category: "soft"
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
    { symbol: "HL", name: "HTML", description: "desc here", category: "soft" },
    { symbol: "SS", name: "SASS", description: "desc here", category: "soft" },
    { symbol: "LS", name: "Less", description: "desc here", category: "soft" },
    { symbol: "CS", name: "CSS", description: "desc here", category: "soft" },
    {
      symbol: "JQ",
      name: "jQuery",
      description: "desc here",
      category: "soft"
    },
    {
      symbol: "BP",
      name: "Bootstrap",
      description: "desc here",
      category: "soft"
    },
    { symbol: "PA", name: "PWA", description: "desc here", category: "soft" },
    { symbol: "RD", name: "RWD", description: "desc here", category: "soft" },
    {
      symbol: "FX",
      name: "Flexbox",
      description: "desc here",
      category: "soft"
    },
    {
      symbol: "MO",
      name: "Magento",
      description: "desc here",
      category: "soft"
    },
    { symbol: "GT", name: "Git", description: "desc here", category: "soft" },
    {
      symbol: "PS",
      name: "Photoshop",
      description: "desc here",
      category: "soft"
    },
    {
      symbol: "AI",
      name: "Illustrator",
      description: "desc here",
      category: "soft"
    },
    { symbol: "MO", name: "MacOS", description: "desc here", category: "soft" },
    { symbol: "JI", name: "JIRA", description: "desc here", category: "soft" },
    { symbol: "SL", name: "Slack", description: "desc here", category: "soft" },
    {
      symbol: "TL",
      name: "Trello",
      description: "desc here",
      category: "soft"
    },

    {
      symbol: "AP",
      name: "Affinity Photo",
      description: "desc here",
      category: "soft"
    },
    {
      symbol: "AD",
      name: "Affinity Designer",
      description: "desc here",
      category: "soft"
    },
    {
      symbol: "SH",
      name: "Sketch",
      description: "desc here",
      category: "soft"
    },
    { symbol: "FI", name: "Figma", description: "desc here", category: "soft" },
    {
      symbol: "ZN",
      name: "Zeplin",
      description: "desc here",
      category: "soft"
    },
    {
      symbol: "RW",
      name: "Remote Work",
      description: "desc here",
      category: "soft"
    },
    {
      symbol: "CH",
      name: "Chatty",
      description: "desc here",
      category: "soft"
    },
    { symbol: "YN", name: "Yarn", description: "desc here", category: "soft" },
    { symbol: "NP", name: "NPM", description: "desc here", category: "soft" },

    { symbol: "GP", name: "Gulp", description: "desc here", category: "soft" },

    {
      symbol: "",
      name: "",
      description: "",
      category: "spacer"
    },
    {
      symbol: "MO",
      name: "Microsoft Office",
      description: "desc here",
      category: "soft"
    },
    { symbol: "EL", name: "Email", description: "desc here", category: "soft" },
    {
      symbol: "GD",
      name: "Good Organised",
      description: "desc here",
      category: "soft"
    },
    {
      symbol: "AE",
      name: "After Effects",
      description: "desc here",
      category: "soft"
    }
  ];
</script>

<style lang="scss">
  .container {
    align-items: center;
    display: flex;
    height: 100%;
    justify-content: center;
    width: 89vw;
  }

  .skillsList {
    display: grid;
    grid-gap: 10px;
    grid-template-columns: repeat(8, 89px);
    justify-content: center;
    margin: auto;
    max-width: 987px;
    padding-left: 0;

    .item {
      border: 2px solid var(--maastricht-blue);
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
      box-sizing: border-box;
      display: flex;
      flex-direction: column;
      height: 89px;
      justify-content: center;
      margin: 8px;
      padding: 8px;
      width: 89px;
      transition: color var(--transition-time),
        border-color var(--transition-time),
        background-color var(--transition-time);

      &:hover {
        &:not(.spacer) {
          background-color: var(--persian-red);
          border-color: var(--persian-red);
          box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16),
            0 3px 6px rgba(0, 0, 0, 0.23);
          color: var(--white);
        }
      }

      &.spacer {
        border: none;
        box-shadow: none;
      }

      .symbol {
        font-size: 34px;
      }

      .name {
        font-size: 13px;
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
      </li>
    {/each}
  </ul>
</div>
