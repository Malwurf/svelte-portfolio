<script>
  import DarkmodeHead from "../darkmode/DarkmodeHead.svelte";
  import { sunIcon, moonIcon } from "../icons/Icons.svelte";

  function changeMode() {
    document.querySelector("body").classList.toggle("darkmode");
  }
</script>

<style lang="scss">
  :global(body.darkmode .switcher svg path) {
    fill: var(--just-black);
  }

  .switcher {
    background-color: var(--just-white);
    border-radius: 50%;
    display: block;
    height: 40px;
    left: 50%;
    margin: 0 auto;
    overflow: hidden;
    position: absolute;
    top: calc(100% - 55px);
    transform: translateX(-50%);
    width: 40px;

    input[type="checkbox"] {
      display: none;
      position: absolute;

      &:checked {
        ~ .icon.sun {
          transform: translate(-50%, 50px);
        }

        ~ .icon.moon {
          transform: translate(-50%, -13px);
        }
      }
    }

    .icon {
      border-radius: 50%;
      box-sizing: border-box;
      display: block;
      height: 27px;
      transition: transform var(--transition-time),
        background var(--transition-time);
      width: 27px;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);

      &.moon {
        transform: translate(-50%, -50px);
      }
    }
  }
</style>

<label class="switcher">
  <input type="checkbox" on:change={changeMode} />
  <span class="icon sun">
    {@html sunIcon}
  </span>

  <span class="icon moon">
    {@html moonIcon}
  </span>
</label>
