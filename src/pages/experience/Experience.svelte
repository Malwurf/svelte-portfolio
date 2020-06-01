<script>
  const jobsList = [
    {
      name: "Divante Sp. z o.o.",
      title: "Frontend Developer",
      description: " ",
      technologies: ["js", "html", "css", "magento", "jquery", "react"],
      clients: [
        "Internal",
        "Enea",
        "Enea - Strefa Zakupów",
        "Open Loyalty",
        "Carrefour",
        "Energa",
        "Distripark"
      ],
      startDate: "03-2018",
      endDate: ""
    },
    {
      name: "Usługi Transportowe K.P.",
      title: "Freelance / Frontend",
      description:
        "Another successful SPA webpage and one of my best clients. Unfortunately, Mr. Krzysztof closed his firm but cooperation was great!",
      technologies: ["html", "scss", "js"],
      clients: ["Owner"],
      startDate: "01-2019",
      endDate: "05-2019"
    },
    {
      name: "BusWojtex",
      title: "Freelance / Frontend",
      description:
        "I did a SPA business-card webpage for a transport company to see how vue.js works - it's cool.",
      technologies: ["vue.js", "sass", "html"],
      clients: ["Owner"],
      startDate: "10-2018",
      endDate: "03-2019"
    },
    {
      name: "Moni - Usługi Krawieckie",
      title: "Freelance / Frontend",
      description:
        "I've designed a brand logo in Adobe Illustrator, created a simple SPA web page, started a fan page on Facebook",
      technologies: ["illustrator", "html", "sass", "js"],
      clients: ["Owner"],
      startDate: "03-2018",
      endDate: "08-2018"
    },
    {
      name: "panaceum.it",
      title: "CEO",
      description: "I've found my own (one-man army) firm!",
      technologies: ["js", "svelte", "scss", "html"],
      clients: [
        "Own Portfolio",
        "Divante",
        "Buswojtex",
        "Moni",
        "Posadzki Ostrowski",
        "Piana Dachy",
        "Washing Machine"
      ],
      startDate: "03-2018",
      endDate: ""
    },
    {
      name: "Stark Industries",
      title: "Jarvis Friend",
      description: "Nope. That's a joke! Sorry :)",
      technologies: ["AI"],
      clients: ["Avengers"],
      startDate: "01-2018",
      endDate: "03-2018"
    },
    {
      name: "Mobile Vikings",
      title: "Freelance / Frontend",
      description:
        "As a subcontractor, I was responsible for implementing the new version of Mobile Vikings Webpage.",
      technologies: ["jquery", "html", "sass", "git"],
      clients: ["Washing Machine"],
      startDate: "04-2017",
      endDate: "08-2017"
    },
    {
      name: "Lemon Sky J. Walter Thompson Poland",
      title: "Frontend Developer",
      description:
        "I was part of Frontend team. Great persons I gained a lot of experience working with them. Most of the time I was making contest pages, integrations with backend (django). Developing RWD in existing / new projects. Finding a solution for business problems f.e. limited page size or loading time. I've worked remotely occasionally.",
      technologies: [
        "js",
        "html",
        "sass",
        "jquery",
        "react",
        "django",
        "emails"
      ],
      clients: [
        "Internal",
        "Winiary",
        "Nowy Styl Group",
        "Wedel",
        "PFR",
        "Prudential",
        "Mazda",
        "Tymbark",
        "Kubuś",
        "Shell",
        "Tiger",
        "Volkswagen",
        "Bols"
      ],
      startDate: "10-2015",
      endDate: "02-2018"
    },
    {
      name: "Red Dragon Media Sp. z o.o.",
      title: "Junior Frontend Developer",
      description:
        "Cutting from project and coding page layout while maintaining certain standards. Implementing mobile versions to existing / new websites. Making animations, using a lot of js libraries for slides, making navigations etc.",
      technologies: ["js", "html", "css", "sass", "jquery"],
      clients: [
        "Tauron",
        "Cooklet",
        "Skyr",
        "Kuchnia Marche",
        "PZU",
        "Danone",
        "emails"
      ],
      startDate: "02-2015",
      endDate: "10-2015"
    },
    {
      name: "WEBDEVPLUS",
      title: "Freelance / Frontend",
      description: "I was part of .",
      technologies: ["js", "html", "css", "jquery", "bootstrap"],
      clients: ["Owner"],
      startDate: "03-2014",
      endDate: "03-2015"
    },
    {
      name: "Freelancer.com",
      title: "Freelance / Frontend",
      description:
        'Implementation of the "Giggzu" website from scratch based on the Photoshop project. I"ve used basic frontend stack - HTML, CSS, Bootstrap 2.',
      technologies: ["js", "html", "css", "bootstrap"],
      clients: ["Giggzu owner"],
      startDate: "10-2014",
      endDate: "11-2014"
    },
    {
      name: "Sygnity S.A.",
      title: "Software Tester",
      description:
        "My second practice. I was responsible for manual and functional testing without software.",
      technologies: [""],
      clients: ["Internal"],
      startDate: "12-2013",
      endDate: "02-2014"
    },
    {
      name: "Next Computers s.c.",
      title: "Computer Specialist",
      description:
        "My practice job on studies. Contact with the client, consulting, sales service, and accepting service orders.",
      technologies: [],
      clients: [],
      startDate: "04-2013",
      endDate: "07-2013"
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

  .jobs-list {
    align-items: flex-start;
    display: flex;
    flex-direction: column;
    list-style: none;
    margin-bottom: 55px;
    margin-top: 55px;
    padding-bottom: 34px;
    padding-left: 0;
    padding-top: 34px;
    position: relative;

    &:after {
      background-color: var(--persian-red);
      bottom: 0;
      content: "";
      left: 50%;
      position: absolute;
      top: 0;
      transform: translateX(-50%);
      width: 3px;
    }

    .item {
      width: 50%;

      .content {
        border: 2px solid var(--maastricht-blue);
        box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
        box-sizing: border-box;
        max-width: 1270px;
        padding: 21px;
        position: relative;
        transition: box-shadow var(--transition-time);
        width: calc(100% - 25px);

        &:hover {
          box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16),
            0 3px 6px rgba(0, 0, 0, 0.23);
        }

        &:before {
          border-color: transparent transparent transparent
            var(--maastricht-blue);
          border-style: solid;
          border-width: 13px 0 13px 13px;
          content: " ";
          display: block;
          height: 0;
          position: absolute;
          right: -13px;
          top: 34px;
          width: 0;
        }

        .headline {
          margin: 0;
        }

        .date {
          color: var(--just-blue);
        }

        .clients {
          font-style: italic;
        }
      }

      &:nth-of-type(even) {
        align-self: flex-end;
        display: flex;
        justify-content: flex-end;

        .content {
          &:before {
            border-color: transparent var(--maastricht-blue) transparent
              transparent;
            border-width: 13px 13px 13px 0;
            left: -13px;
            right: auto;
          }
        }
      }
    }
  }

  @media all and (max-width: 1023px) {
    .jobs-list {
      &:after {
        display: none;
      }

      .item {
        margin-bottom: 0px;
        position: relative;
        width: 89%;

        & + .item {
          margin-top: 34px;
        }

        &:nth-of-type(even) {
          align-self: flex-start;
          .content {
            &:before {
              border-width: 0 13px 13px 13px;
              border-color: transparent transparent var(--persian-red)
                transparent;
              left: 50%;
              transform: translateX(-50%);
              right: auto;
              top: -13px;
            }
          }
        }

        .content {
          width: 100%;

          &:before {
            border-width: 0 13px 13px 13px;
            border-color: transparent transparent var(--persian-red) transparent;
            left: 50%;
            transform: translateX(-50%);
            right: auto;
            top: -13px;
          }
        }
      }
    }
  }
</style>

<div class="container">
  <ul class="jobs-list">
    {#each jobsList as job}
      <li class="item">
        <div class="content">
          <h2 class="headline">{job.name}</h2>
          <div class="description">
            <p>{job.title}</p>
            <p>
              {@html job.description}
            </p>
            <p class="clients">Clients - {job.clients.join(', ')}</p>
            <p>{job.technologies.join(', ')}</p>
          </div>
          <div class="date">{job.startDate} - {job.endDate}</div>
        </div>
      </li>
    {/each}
  </ul>
</div>
