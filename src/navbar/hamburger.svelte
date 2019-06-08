<style lang="scss">
nav {
  align-items: center;
  background-color: var(--sauvignon-white);
  display: flex;
  height: 100vh;
  justify-content: center;
  width: 80px;
}

.trigger {
  align-items: center;
  display: flex;
  flex-direction: column;
  height: 70px;
  justify-content: center;
  margin: 0 auto;
  width: 70px;

  input[type='checkbox'] {
    display:none;
  }

  input[type='checkbox']:checked {
    ~ label {
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
          box-shadow: 1px 0px 5px 2px var(--crimson-red);
        }
      }

      &:nth-of-type(2) {
        transform: rotateZ(675deg) translateX(-20px) translateY(-10px);

        &::after {
          box-shadow: 1px 0px 5px 2px var(--corbeau-blue);
        }
      }

      &:nth-of-type(3) {
        transform: rotateZ(-495deg) translateX(-9px) translateY(16px);

        &::after {
          box-shadow: 1px 0px 5px 2px var(--brightlettuce-green);
        }
      }
    }
  }

  label {
    background-color: var(--corbeau-blue);
    cursor: pointer;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    height: 4px;
    width: 10%;
    position: relative;
    left: -10px;
    transform-origin: center;
    
    &::before {
      content: '';
      height: 4px;
      background-color: var(--corbeau-blue);
      display: block;
      position: relative;
      left: 8px;
      min-width: 13px;
    }

    &::after {
      background-color: var(--corbeau-blue);
      content: '';
      display: block;
      height: 4px;
      min-width: 30px;
      position: relative;
      right: -12px;
      transition: box-shadow var(--transition-time);
    }

    &:nth-of-type(2) {
      transform: rotateZ(180deg);
      right: -10px;
      left: auto;
    }

    & + label {
      margin-top: 8px;
    }
  }
}
</style>

<nav>
  <div class="trigger">
    <input type="checkbox" name="" id="NavigationSwitcher" />
    <label for="NavigationSwitcher" />
    <label for="NavigationSwitcher" />
    <label for="NavigationSwitcher" />
  </div>
</nav>
