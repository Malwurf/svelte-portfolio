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
      endDate: "",
      opinion: false
    },
    {
      name: "Personal Trainer M.B.",
      title: "Freelance / Graphic Designer",
      description: "I've designed leaflets for Michał B. - personal trainer.",
      technologies: ["affinity designer"],
      clients: ["Owner"],
      startDate: "03-2019",
      endDate: "03-2019",
      opinion: false
    },
    {
      name: "Usługi Transportowe K.P.",
      title: "Freelance / Frontend",
      description:
        "Another successful SPA webpage and one of my best clients. Unfortunately, Mr. Krzysztof closed his firm but cooperation was great!",
      technologies: ["html", "scss", "js"],
      clients: ["Owner"],
      startDate: "01-2019",
      endDate: "05-2019",
      opinion: false
    },
    {
      name: "BusWojtex",
      title: "Freelance / Frontend",
      description:
        "I did a SPA business-card webpage for a transport company to see how vue.js works - it's cool.",
      technologies: ["vue.js", "sass", "html"],
      clients: ["Owner"],
      startDate: "10-2018",
      endDate: "03-2019",
      opinion: false
    },
    {
      name: "Moni - Usługi Krawieckie",
      title: "Freelance / Frontend",
      description:
        "I've designed a brand logo in Adobe Illustrator, created a simple SPA web page, started a fan page on Facebook",
      technologies: ["illustrator", "html", "sass", "js"],
      clients: ["Owner"],
      startDate: "03-2018",
      endDate: "08-2018",
      opinion: false
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
      endDate: "",
      opinion: false
    },
    {
      name: "Stark Industries",
      title: "Jarvis Friend",
      description: "Nope. That's a joke! Sorry :)",
      technologies: ["AI"],
      clients: ["Avengers"],
      startDate: "01-2018",
      endDate: "03-2018",
      opinion: false
    },
    {
      name: "Mobile Vikings",
      title: "Freelance / Frontend",
      description:
        "As a subcontractor, I was responsible for implementing the new version of Mobile Vikings Webpage.",
      technologies: ["jquery", "html", "sass", "git"],
      clients: ["Washing Machine"],
      startDate: "04-2017",
      endDate: "08-2017",
      opinion: false
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
      endDate: "02-2018",
      opinion: true
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
      endDate: "10-2015",
      opinion: false
    },
    {
      name: "WUL-KAM K.W.",
      title: "Freelance / Graphic Designer",
      description:
        "I've designed visit cards for the best vulcanization firm near Legnica",
      technologies: ["Illustrator", "Photoshop"],
      clients: ["Owner"],
      startDate: "01-2015",
      endDate: "02-2015",
      opinion: false
    },
    {
      name: "WEBDEVPLUS",
      title: "Freelance / Frontend",
      description: "I was part of .",
      technologies: ["js", "html", "css", "jquery", "bootstrap"],
      clients: ["Owner"],
      startDate: "03-2014",
      endDate: "03-2015",
      opinion: false
    },
    {
      name: "Freelancer.com",
      title: "Freelance / Frontend",
      description:
        'Implementation of the "Giggzu" website from scratch based on the Photoshop project. I"ve used basic frontend stack - HTML, CSS, Bootstrap 2.',
      technologies: ["js", "html", "css", "bootstrap"],
      clients: ["Giggzu owner"],
      startDate: "10-2014",
      endDate: "11-2014",
      opinion: false
    },
    {
      name: "Sygnity S.A.",
      title: "Software Tester",
      description:
        "My second practice. I was responsible for manual and functional testing without software.",
      technologies: [""],
      clients: ["Internal"],
      startDate: "12-2013",
      endDate: "02-2014",
      opinion: false
    },
    {
      name: "Next Computers s.c.",
      title: "Computer Specialist",
      description:
        "My practice job on studies. Contact with the client, consulting, sales service, and accepting service orders.",
      technologies: [],
      clients: [],
      startDate: "04-2013",
      endDate: "07-2013",
      opinion: false
    }
  ];

  function opinionLink(name) {
    let link = "opinions/" + name.toLowerCase().replace(/[\s\.]/g, "") + ".pdf";
    return link;
  }
</script>

<style lang="scss">
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
      &:after {
        background-color: var(--pegasus-red);
        bottom: 0;
        content: "";
        left: 50%;
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

          @media all and (min-width: 768px) {
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

<div class="container">
  <ul class="jobs-list">
    {#each jobsList as job}
      <li class="item">
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
