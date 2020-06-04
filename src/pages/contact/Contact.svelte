<script>
  import Selfie from "./Selfie.svelte";

  const bitcoinIcon =
    '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path d="M256.198 0C114.804-.119.119 114.408 0 255.802S114.408 511.881 255.802 512c141.375-.119 255.98-114.625 256.198-256C512 114.685 397.513.119 256.198 0zm-.396 469.4c-117.855 0-213.399-95.545-213.399-213.4S137.947 42.601 255.802 42.601c117.815.119 213.28 95.584 213.399 213.399 0 117.855-95.544 213.4-213.399 213.4z" /> <path d="M324.954 243.517c17.12-9.65 26.373-28.968 23.183-48.347-3.963-29.919-39.628-41.214-67.765-43.591v-44.978h-27.74v44.582h-18.625v-44.582h-27.74v44.582H150.39v28.731h20.805c9.313 0 13.87 2.774 13.87 10.303V313.66c0 10.303-5.152 13.474-10.7 13.474h-21.201v29.325h53.895v45.573h27.938v-45.573h18.625v45.573h27.146v-45.573h5.944c57.065 0 76.087-27.938 76.087-65.981-.456-22.431-16.01-41.73-37.845-46.961zm-90.948-61.82h19.814c13.87 0 41.214 2.378 41.214 24.966.951 14.742-9.729 27.661-24.372 29.523h-36.656v-54.489zm30.712 142.662v-.198h-30.712v-59.443h35.666c8.322 0 39.628 2.774 39.628 24.966s-14.86 34.675-44.582 34.675z" /></svg>';
  const emailIcon =
    '<svg viewBox="0 0 479.058 479.058" xmlns="http://www.w3.org/2000/svg"><path d="M434.146 59.882H44.912C20.146 59.882 0 80.028 0 104.794v269.47c0 24.766 20.146 44.912 44.912 44.912h389.234c24.766 0 44.912-20.146 44.912-44.912v-269.47c0-24.766-20.146-44.912-44.912-44.912zm0 29.941c2.034 0 3.969.422 5.738 1.159L239.529 264.631 39.173 90.982a14.902 14.902 0 015.738-1.159zm0 299.411H44.912c-8.26 0-14.971-6.71-14.971-14.971V122.615l199.778 173.141c2.822 2.441 6.316 3.655 9.81 3.655s6.988-1.213 9.81-3.655l199.778-173.141v251.649c-.001 8.26-6.711 14.97-14.971 14.97z" /></svg>';
  const smartphoneIcon =
    '<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"><path d="M298.667 25.6h-85.333a8.536 8.536 0 00-8.533 8.533 8.536 8.536 0 008.533 8.533h85.333a8.536 8.536 0 008.533-8.533 8.536 8.536 0 00-8.533-8.533zM358.4 25.6h-8.533a8.536 8.536 0 00-8.533 8.533 8.536 8.536 0 008.533 8.533h8.533a8.536 8.536 0 008.533-8.533A8.536 8.536 0 00358.4 25.6zM266.598 435.2H245.41c-12.979 0-23.543 10.564-23.543 23.543v4.122c0 12.979 10.564 23.535 23.535 23.535h21.188c12.979 0 23.543-10.556 23.543-23.535v-4.122c0-12.979-10.564-23.543-23.535-23.543zm6.469 27.665a6.475 6.475 0 01-6.468 6.468H245.41c-3.575 0-6.477-2.901-6.477-6.468v-4.122a6.48 6.48 0 016.477-6.477h21.18a6.478 6.478 0 016.477 6.477v4.122z" /><path d="M370.227 0H141.781c-17.007 0-30.848 13.841-30.848 30.848v450.304c0 17.007 13.841 30.848 30.848 30.848h228.437c17.007 0 30.848-13.841 30.848-30.839V30.848C401.067 13.841 387.226 0 370.227 0zM384 481.152c0 7.595-6.178 13.781-13.773 13.781H141.781c-7.603 0-13.781-6.187-13.781-13.773V30.848c0-7.595 6.178-13.781 13.781-13.781h228.437c7.603 0 13.781 6.187 13.781 13.781v450.304z" /><path d="M392.533 51.2H119.467a8.536 8.536 0 00-8.533 8.533v358.4a8.536 8.536 0 008.533 8.533h273.067a8.536 8.536 0 008.533-8.533v-358.4c0-4.71-3.823-8.533-8.534-8.533zM384 409.6H128V68.267h256V409.6z"></svg>';
  const twitterIcon =
    '<svg viewBox="0 -47 512 512" xmlns="http://www.w3.org/2000/svg"><path d="M512 55.965c-32.207 1.484-31.504 1.363-35.145 1.668L495.93 3.16s-59.54 21.902-74.633 25.82c-39.64-35.628-98.563-37.203-140.688-11.312-34.496 21.207-53.011 57.625-46.836 100.191C166.637 108.543 110.07 76.72 65.41 23.07L51.285 6.105 40.73 25.488C27.39 49.98 22.96 77.984 28.254 104.34A113.287 113.287 0 0039.23 135.12l-12.117-4.695-1.437 20.246c-1.457 20.566 5.39 44.574 18.32 64.215a114.185 114.185 0 0014.27 17.597l-6.262-.96 7.64 23.199c10.043 30.48 30.903 54.062 57.973 67.172-27.035 11.472-48.875 18.793-84.773 30.601L0 363.293l30.336 16.586c11.566 6.324 52.437 27.445 92.82 33.781 89.766 14.078 190.832 2.613 258.871-58.664 57.309-51.613 76.114-125.031 72.207-201.433-.59-11.567 2.579-22.606 8.922-31.079 12.707-16.964 48.766-66.406 48.844-66.52zm-72.832 48.55c-10.535 14.067-15.813 32.032-14.867 50.579 3.941 77.066-17.028 136.832-62.328 177.629-52.918 47.66-138.274 66.367-234.172 51.324-17.367-2.723-35.317-8.82-50.172-14.91 30.098-10.356 53.34-19.586 90.875-37.352l52.398-24.8-57.851-3.704c-27.711-1.773-50.785-15.203-64.969-37.008a103.763 103.763 0 0022.023-3.671l55.176-15.368-55.636-13.625c-27.036-6.62-42.446-22.797-50.614-35.203-5.363-8.152-8.867-16.504-10.969-24.203 5.579 1.496 12.083 2.563 22.57 3.602l51.497 5.093-40.8-31.828c-29.4-22.93-41.18-57.379-32.544-90.496 91.75 95.164 199.477 88.012 210.32 90.528-2.386-23.184-2.449-23.239-3.074-25.446-13.886-49.09 16.547-74.015 30.274-82.453 28.672-17.621 74.183-20.277 105.707 8.754 6.808 6.266 16.015 8.73 24.633 6.59 7.734-1.922 14.082-3.957 20.296-6.172L434.004 89.32l16.516.012a8240.32 8240.32 0 01-11.352 15.184zm0 0" /> </svg>';
  const linkedinIcon =
    '<svg viewBox="-28 0 512 512.001" xmlns="http://www.w3.org/2000/svg"><path d="M104.36 151.625H18.046C8.37 151.625.5 159.496.5 169.172v325.285C.5 504.129 8.371 512 18.047 512h86.312c9.672 0 17.543-7.871 17.543-17.543V169.172c0-9.676-7.87-17.547-17.543-17.547zm-12.5 330.332H30.542V181.668h61.316zm0 0M61.203 0C27.453 0 0 27.453 0 61.2c0 33.75 27.453 61.202 61.203 61.202 33.742 0 61.2-27.453 61.2-61.203C122.402 27.453 94.948 0 61.202 0zm0 92.36c-17.183 0-31.16-13.977-31.16-31.16 0-17.18 13.977-31.157 31.16-31.157 17.18 0 31.156 13.977 31.156 31.156 0 17.18-13.976 31.16-31.156 31.16zm0 0M401.047 189.762c-20.633-17.223-46.863-26.434-73.832-25.934a113.183 113.183 0 00-47.95 11.66v-7.101c0-9.254-7.503-16.758-16.757-16.758h-87.883c-9.254 0-16.758 7.504-16.758 16.758v326.855c0 9.258 7.504 16.758 16.758 16.758h89.617c8.297 0 15.024-6.727 15.024-15.02V302.102c0-16.684 13.054-30.801 29.726-31.297 17.328-.512 31.586 13.43 31.586 30.644v195.844c0 8.121 6.586 14.707 14.707 14.707h86.13c8.12 0 14.706-6.586 14.706-14.707V307.406c0-45.547-20.074-88.43-55.074-117.644zm25.031 292.195h-55.453V301.449c0-33.469-27.23-60.699-60.703-60.699-33.469 0-60.7 27.23-60.7 60.7v180.507H187.91V181.668h61.313V203.5h.02a14.948 14.948 0 003.757 9.957c5.496 6.211 14.992 6.79 21.203 1.29a83.224 83.224 0 0153.567-20.884c19.761-.375 38.94 6.367 54.027 18.961 28.144 23.492 44.281 57.965 44.281 94.582zm0 0" /></svg>';
  const messangerIcon =
    '<svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M3.424 23.25c0 .574.618.933 1.118.654l4.091-2.303c3.784 1.024 7.851.271 10.943-2.036C22.387 17.468 24 14.354 24 11.022 24 4.944 18.617 0 12 0S0 4.944 0 11.022c0 2.916 1.213 5.637 3.424 7.699zM1.5 11.022C1.5 5.771 6.21 1.5 12 1.5s10.5 4.271 10.5 9.522c0 2.854-1.393 5.53-3.821 7.341-2.799 2.087-6.512 2.728-9.928 1.712a.753.753 0 00-.582.065l-3.246 1.827v-3.579a.752.752 0 00-.254-.563C2.625 16.027 1.5 13.611 1.5 11.022z" /> <path d="M4.835 15.171l5.509-2.755 2.618 2.69c.343.353.82.258 1.072.004l6-6.083c.595-.604-.12-1.58-.875-1.195l-5.509 2.812-2.614-2.669A.749.749 0 009.97 7.97l-6 6c-.6.6.11 1.58.865 1.201zm5.66-5.605l2.47 2.521c.23.235.586.292.876.143l1.866-.952-2.203 2.233-2.466-2.535a.75.75 0 00-.873-.148l-1.866.933z" /></svg>';

  const githubIcon =
    '<svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M.184 10.462c-.779 4.906 1.401 10.823 8.123 13.006.12.022.231.032.335.032.782 0 1.32-.582 1.32-1.3-.097-.523.383-2.642-.92-2.357-2.519.536-2.821-.871-3.205-1.607 1.086 1.394 2.718 1.359 3.949.819.683-.3.326-1.064.65-1.343a.75.75 0 00-.407-1.314c-2.314-.255-4.457-1.001-4.457-4.702 0-2.168 1.505-2.362 1.09-3.269-.015-.033-.333-.754-.045-1.849 1.419.262 2.072 1.28 2.753 1.097 1.687-.46 3.544-.46 5.23 0 .704.189 1.207-.801 2.738-1.103.441 1.654-.473 2.058.103 2.677.632.68.953 1.503.953 2.447 0 5.564-4.717 3.957-5.101 5.22a.748.748 0 00.235.792c.61.513.53 1.83.465 2.889-.067 1.098-.125 2.045.482 2.579.214.19.595.393 1.284.253 6.634-2.131 8.83-8.022 8.063-12.917C21.726-2.856 2.296-2.84.184 10.462zm8.27 10.978l.004.505a11.811 11.811 0 01-1.475-.623c.425.109.913.156 1.471.118zm.37-3.7l-.015.08c-.853.252-1.509.001-1.957-.752l-.001-.002c.68.364 1.381.56 1.973.674zM12 2c11.833 0 14.502 16.267 3.469 19.941-.038-.297-.003-.857.021-1.252.058-.951.126-2.059-.213-2.985 5.088-1.059 5.513-6.646 3.554-9.135.243-.952.145-3.189-.729-3.463-.206-.065-1.305-.304-3.437 1.037a11.657 11.657 0 00-5.361 0c-1.064-.667-3.462-1.752-3.922-.6-.534 1.342-.407 2.427-.248 3.03-1.739 2.204-1.218 5.894.534 7.626-.993-.475-2.361-.637-2.656.314-.323 1.037.912.911 1.679 2.804.073.236.208.513.415.788C-1.705 14.54 1.581 2 12 2z"/></svg>';

  let description = "";
  let showDescriptionBox = false;

  function showDescription(buttonName) {
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
  }
</script>

<style lang="scss">
  div :global(.dynamic.link) {
    color: var(--pegasus-red);
    font-weight: bolder;
    text-decoration: none;
  }

  div :global(.contact-details) {
    color: var(--bleachedsilk-white);
  }

  div :global(button:active svg path, button:focus svg path) {
    fill: var(--pegasus-red);
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
    background-color: var(--white);
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 21px;
    position: relative;
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

      .link {
        display: block;
        height: 34px;
        width: 34px;
      }
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

    .link {
      color: var(--pegasus-red);
      text-decoration: none;
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

<h1 class="page-headline">Contact</h1>

<div class="container">
  <section class="contact-card">
    <div class="contact-info">
      <Selfie />
      <div class="name">Przemysław Korościk</div>

      <ul class="icons-list">
        <li class="item">
          <button on:click={() => showDescription('email')}>
            {@html emailIcon}
          </button>
        </li>
        <li class="item">
          <button on:click={() => showDescription('phone')}>
            {@html smartphoneIcon}
          </button>
        </li>
        <li class="item">
          <button on:click={() => showDescription('github')}>
            {@html githubIcon}
          </button>
        </li>
        <li class="item">
          <button on:click={() => showDescription('linkedin')}>
            {@html linkedinIcon}
          </button>
        </li>
        <li class="item">
          <button on:click={() => showDescription('messanger')}>
            {@html messangerIcon}
          </button>
        </li>
        <li class="item">
          <button on:click={() => showDescription('donate')}>
            {@html bitcoinIcon}
          </button>
        </li>
      </ul>
    </div>

    <div class="contact-details" class:active={showDescriptionBox}>
      <p>
        {@html description}
      </p>
    </div>
  </section>

</div>
