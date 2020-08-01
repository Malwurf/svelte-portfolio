<script>
  export let isChecked;
</script>

<div>
  <label class="trigger">
    <input type="checkbox" bind:checked={isChecked} on:change />
    <span for="NavigationTrigger" />
    <span for="NavigationTrigger" />
    <span for="NavigationTrigger" />
  </label>
</div>

<style lang="scss">
  .trigger {
    align-items: center;
    cursor: pointer;
    display: flex;
    flex-direction: column;
    height: var(--navigation-width);
    justify-content: center;
    margin: 0 auto;
    width: var(--navigation-width);

    input[type="checkbox"] {
      display: none;
    }

    input[type="checkbox"]:checked {
      ~ span {
        transition: transform var(--transition-time);

        &::after {
          background-color: var(--just-white);
          border-radius: 0 4px 4px 0;
          min-width: 40px;
        }

        &::before {
          min-width: 10px;
        }

        &:nth-of-type(1) {
          transform: rotateZ(450deg) translateX(-3px) translateY(-8px);

          &::after {
            box-shadow: 1px 0 5px 2px var(--pegasus-red);
          }
        }

        &:nth-of-type(2) {
          transform: rotateZ(675deg) translateX(-20px) translateY(-10px);

          &::after {
            box-shadow: 1px 0 5px 2px var(--just-blue);
          }
        }

        &:nth-of-type(3) {
          transform: rotateZ(-495deg) translateX(-9px) translateY(16px);

          &::after {
            box-shadow: 1px 0 5px 2px var(--brightlettuce-green);
          }
        }
      }
    }

    span {
      align-items: center;
      background-color: var(--just-white);
      display: flex;
      flex-direction: row;
      height: 4px;
      justify-content: center;
      left: -10px;
      position: relative;
      transform-origin: center;
      width: 10%;

      &::before {
        background-color: var(--just-white);
        content: "";
        display: block;
        height: 4px;
        left: 8px;
        min-width: 13px;
        position: relative;
      }

      &::after {
        background-color: var(--just-white);
        content: "";
        display: block;
        height: 4px;
        min-width: 30px;
        position: relative;
        right: -12px;
        transition: box-shadow var(--transition-time);
      }

      &:nth-of-type(2) {
        left: auto;
        right: -10px;
        transform: rotateZ(180deg);
      }

      & + span {
        margin-top: 8px;
      }
    }
  }
</style>
