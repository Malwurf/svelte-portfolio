<script>
  const jobsList = [
    {
      name: "Next Computers s.c.",
      title: "Computer Specialist",
      description: "Naprawiacz sprzętu.",
      technologies: [],
      clients: [],
      startDate: "04-2013",
      endDate: "07-2013"
    },
    {
      name: "Sygnity S.A.",
      title: "Software Tester",
      description: "Desc",
      technologies: ["js", "html", "css"],
      clients: ["Hulk", "Ant-man"],
      startDate: "12-2013",
      endDate: "02-2014"
    },
    {
      name: "Freelancer.com",
      title: "Frontend Ninja",
      description:
        "Volvitur ingreditur id ait mea vero cum autem quod ait Cumque ego illum vero cum unde beata. Commendavi si non dum est in. Dionysiadem tuos ratio puella ut casus, tunc lacrimas effunditis magister cives Tharsis. Puellae addita verbaque capellam sanctissima quid, apollinem existimas filiam rex cum autem quod tamen adnuente rediens eam est se in. Peracta licet ad nomine Maria non ait in modo compungi mulierem volutpat.",
      technologies: ["js", "html", "css"],
      clients: ["Hulk", "Ant-man"],
      startDate: "10-2014",
      endDate: "11-2014"
    },
    {
      name: "WEBDEVPLUS",
      title: "Frontend Ninja",
      description:
        "Volvitur ingreditur id ait mea vero cum autem quod ait Cumque ego illum vero cum unde beata. Commendavi si non dum est in. Dionysiadem tuos ratio puella ut casus, tunc lacrimas effunditis magister cives Tharsis. Puellae addita verbaque capellam sanctissima quid, apollinem existimas filiam rex cum autem quod tamen adnuente rediens eam est se in. Peracta licet ad nomine Maria non ait in modo compungi mulierem volutpat.",
      technologies: ["js", "html", "css"],
      clients: ["Hulk", "Ant-man"],
      startDate: "03-2014",
      endDate: "03-2015"
    },
    {
      name: "Red Dragon Media Sp. z o.o.",
      title: "Frontend Ninja",
      description:
        "Volvitur ingreditur id ait mea vero cum autem quod ait Cumque ego illum vero cum unde beata. Commendavi si non dum est in. Dionysiadem tuos ratio puella ut casus, tunc lacrimas effunditis magister cives Tharsis. Puellae addita verbaque capellam sanctissima quid, apollinem existimas filiam rex cum autem quod tamen adnuente rediens eam est se in. Peracta licet ad nomine Maria non ait in modo compungi mulierem volutpat.",
      technologies: ["js", "html", "css"],
      clients: ["Hulk", "Ant-man"],
      startDate: "02-2015",
      endDate: "10-2015"
    },
    {
      name: "Lemon Sky J. Walter Thompson Poland",
      title: "Junior Frontend Developer",
      description:
        "Volvitur ingreditur id ait mea vero cum autem quod ait Cumque ego illum vero cum unde beata. Commendavi si non dum est in. Dionysiadem tuos ratio puella ut casus, tunc lacrimas effunditis magister cives Tharsis. Puellae addita verbaque capellam sanctissima quid, apollinem existimas filiam rex cum autem quod tamen adnuente rediens eam est se in. Peracta licet ad nomine Maria non ait in modo compungi mulierem volutpat.",
      technologies: ["js", "html", "css"],
      clients: ["Hulk", "Ant-man"],
      startDate: "10-2015",
      endDate: "07-2017"
    },
    {
      name: "Lemon Sky J. Walter Thompson Poland",
      title: "Frontend Developer",
      description:
        "Volvitur ingreditur id ait mea vero cum autem quod ait Cumque ego illum vero cum unde beata. Commendavi si non dum est in. Dionysiadem tuos ratio puella ut casus, tunc lacrimas effunditis magister cives Tharsis. Puellae addita verbaque capellam sanctissima quid, apollinem existimas filiam rex cum autem quod tamen adnuente rediens eam est se in. Peracta licet ad nomine Maria non ait in modo compungi mulierem volutpat.",
      technologies: ["js", "html", "css"],
      clients: ["Hulk", "Ant-man"],
      startDate: "07-2017",
      endDate: "02-2018"
    },
    {
      name: "panaceum.it",
      title: "CEO",
      description: "I've founded my own one person army company!",
      technologies: ["js", "html", "css"],
      clients: ["Hulk", "Ant-man"],
      startDate: "03-2018",
      endDate: ""
    },
    {
      name: "Divante Sp. z o.o.",
      title: "Frontend Developer",
      description:
        "Volvitur ingreditur id ait mea vero cum autem quod ait Cumque ego illum vero cum unde beata. Commendavi si non dum est in. Dionysiadem tuos ratio puella ut casus, tunc lacrimas effunditis magister cives Tharsis. Puellae addita verbaque capellam sanctissima quid, apollinem existimas filiam rex cum autem quod tamen adnuente rediens eam est se in. Peracta licet ad nomine Maria non ait in modo compungi mulierem volutpat.",
      technologies: ["js", "html", "css"],
      clients: ["Hulk", "Ant-man"],
      startDate: "03-2018",
      endDate: ""
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
      background: var(--persian-red);
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
        position: relative;
        width: calc(100% - 25px);
        box-sizing: border-box;
        padding: 8px;
        transition: box-shadow var(--transition-time);

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

  @media (max-width: 1023px) {
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
              border-width: 13px 13px 0 13px;
              border-color: var(--maastricht-blue) transparent transparent
                transparent;
              left: 50%;
              transform: translateX(-50%);
              right: auto;
              top: 100%;
            }
          }
        }

        .content {
          width: 100%;

          &:before {
            border-width: 13px 13px 0 13px;
            border-color: var(--maastricht-blue) transparent transparent
              transparent;
            left: 50%;
            transform: translateX(-50%);
            right: auto;
            top: 100%;
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
            <p>{job.description}</p>
            <p>{job.clients}</p>
            <p>{job.technologies}</p>
          </div>
          <div class="date">{job.startDate} - {job.endDate}</div>
        </div>
      </li>
    {/each}
  </ul>
</div>
