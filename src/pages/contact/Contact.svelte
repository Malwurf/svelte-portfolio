<script>
  import PageHeadline from "../../pageheadline/PageHeadline.svelte";
  import Selfie from "./Selfie.svelte";
  import { iconsList } from "./IconsList.svelte";

  const name = "Przemysław Korościk";
  const headline = "Contact";

  let description = "";
  let showDescriptionBox = false;

  const showDescription = (buttonName) => {
    showDescriptionBox = true;

    switch (buttonName) {
      case "email":
        description =
          'Feel free to send me a message <a href="mailto:przemyslaw.koroscik@gmail.com" class="dynamic link">przemyslaw.koroscik@gmail.com</a>.';
        break;

      case "phone":
        description = `<p>If you're developer, You know where to find it.</p>
          <p>If you're not... ask developer ;)</p>
          <p>If you're on mobile device... just send me an email :)</p>`;
        console.log("Call me - +48 889 788 888");
        break;

      case "donate":
        description = `<p>Feel free to send me some donations! Your money will be happier with me!</p>
          <p>Revolut - +48 889 788 888</p>
          <p>BTC - 34Gk63x1d6QmLBXmsu4RsanvSXW8LxjzDC</p>
          <p>ETH - 0x38F7a8C5a607415BFBDeD33C5b0927008465Ba70`;
        break;

      case "github":
        description = `Most of my projects are commercial, so I don't have rich my own portfolio BUT I work on it <a href="https://github.com/Malwurf?tab=repositories." target="_blank" class="dynamic link">@Malwurf</a>`;
        break;

      case "linkedin":
        description =
          'Here we can connect at LinkedIn portal <a href="https://www.linkedin.com/in/przemek-krecik" target="_blank" class="dynamic link">Przemysław Korościk</a>.';
        break;

      case "messanger":
        description =
          'Send me a direct message <a href="http://m.me/kreciik.krecik" target="_blank" class="dynamic link">Przemysław Korościk</a>.';
        break;

      default:
        "";
    }
  };
</script>

<PageHeadline {headline} />

<div class="container">
  <section class="contact-card">
    <div class="contact-info">

      <Selfie />

      <div class="name target">{name}</div>

      <ul class="icons-list">

        {#each iconsList as item}
          <li class="item target">
            <button on:click={() => showDescription(item.description)}>
              {@html item.icon}
            </button>
          </li>
        {/each}

      </ul>
    </div>

    <div class="contact-details" class:active={showDescriptionBox}>
      <p>
        {@html description}
      </p>
    </div>
  </section>

</div>

<style lang="scss">
  :global(.dynamic.link) {
    color: var(--pegasus-red);
    font-weight: bolder;
    text-decoration: none;
  }

  :global(.contact-details) {
    color: var(--just-white);
  }

  :global(button:active svg path, button:focus svg path) {
    fill: var(--pegasus-red);
  }

  :global(body.darkmode) {
    .contact-card {
      box-shadow: 0 -3px 6px rgba(217, 4, 4, 0.55),
        0 3px 6px rgba(217, 4, 4, 0.89);

      &:hover {
        .contact-details.active {
          box-shadow: 0 0 3px rgba(217, 4, 4, 0.55),
            0 2px 9px rgba(217, 4, 4, 0.89);
        }
      }
    }

    .contact-info {
      background-color: var(--almost-black);
    }

    .contact-details.active {
      box-shadow: 0 0 3px rgba(217, 4, 4, 0.55), 0 2px 9px rgba(217, 4, 4, 0.89);
    }
  }

  .contact-card {
    box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
    position: relative;
    transition: box-shadow var(--transition-time);
    max-width: 610px;
    width: 100%;

    @media all and (min-width: 1024px) {
      &:hover {
        box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);

        .contact-details.active {
          box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16),
            0 3px 6px rgba(0, 0, 0, 0.23);
        }
      }
    }
  }

  .contact-info {
    align-items: center;
    background-color: var(--just-white);
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 21px;
    position: relative;
    transition: background-color var(--transition-time);
    width: 100%;
    z-index: 1;

    @media all and (min-width: 640px) {
      padding: 34px;
    }

    .name {
      text-align: center;
      font-size: 21px;
    }

    .icons-list {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      list-style: none;
      max-width: 233px;
      padding-left: 0;
      width: 100%;
    }
  }

  .contact-details {
    background-color: var(--maastricht-blue);
    box-sizing: border-box;
    padding: 13px;
    transform: translateY(-100%);
    transition: transform var(--transition-time),
      box-shadow var(--transition-time);
    width: 100%;
    word-wrap: break-word;

    @media (hover: hover) and (pointer: fine) and (min-width: 768px) {
      position: absolute;
      top: 100%;
    }

    &.active {
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
      transform: translateY(0);
    }
  }

  button {
    background-color: transparent;
    border-radius: 50%;
    border: 1px solid transparent;
    cursor: pointer;
    height: 69px;
    padding: 10px;
    position: relative;
    width: 69px;

    &:active,
    &:focus {
      outline: 0;
    }
  }
</style>
