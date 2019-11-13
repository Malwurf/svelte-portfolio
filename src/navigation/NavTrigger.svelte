<script>

</script>

<style lang="scss">
  .wrapper {
    align-items: center;
    background-color: var(--sauvignon-white);
    display: flex;
    height: 100vh;
    justify-content: center;
    position: relative;
    z-index: 3;
  }
  .trigger {
    align-items: center;
    display: flex;
    flex-direction: column;
    height: 70px;
    justify-content: center;
    margin: 0 auto;
    width: 70px;

    input[type="checkbox"] {
      display: none;
    }

    input[type="checkbox"]:checked {
      ~ span {
        transition: transform var(--transition-time);

        &::after {
          background-color: var(--white);
          border-radius: 0 4px 4px 0;
          min-width: 40px;
        }

        &::before {
          min-width: 10px;
        }

        &:nth-of-type(1) {
          transform: rotateZ(450deg) translateX(-3px) translateY(-8px);

          &::after {
            box-shadow: 1px 0 5px 2px var(--crimson-red);
          }
        }

        &:nth-of-type(2) {
          transform: rotateZ(675deg) translateX(-20px) translateY(-10px);

          &::after {
            box-shadow: 1px 0 5px 2px var(--corbeau-blue);
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
      background-color: var(--corbeau-blue);
      cursor: pointer;
      display: flex;
      flex-direction: row;
      height: 4px;
      justify-content: center;
      left: -10px;
      position: relative;
      transform-origin: center;
      width: 10%;

      &::before {
        background-color: var(--corbeau-blue);
        content: "";
        display: block;
        height: 4px;
        left: 8px;
        min-width: 13px;
        position: relative;
      }

      &::after {
        background-color: var(--corbeau-blue);
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

<div class="wrapper">
  <label class="trigger">
    <input
      type="checkbox"
      name="NavigationTrigger"
      id="NavigationTrigger"
      on:change />
    <span for="NavigationTrigger" />
    <span for="NavigationTrigger" />
    <span for="NavigationTrigger" />
  </label>
</div>
