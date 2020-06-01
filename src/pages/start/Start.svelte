<script>
  const whoAmI = "I am Przemek";
  const jobTitle = "< Call me Krecik />";
</script>

<style lang="scss">
  .container {
    align-items: center;
    display: flex;
    height: 100%;
    justify-content: center;
    width: 89vw;

    .headlines {
      @media screen and (min-width: 768px) and (max-width: 1024px) {
        margin-left: 21px;
      }
    }

    .headline {
      font-size: 34px;
      margin: 0;

      @media screen and (min-width: 768px) {
        font-size: 130px;
      }

      &.hello {
        align-items: flex-end;
        display: flex;
        line-height: 21px;

        @media screen and (min-width: 768px) {
          line-height: 89px;
        }
      }

      & + .headline {
        margin-top: 8px;

        @media screen and (min-width: 768px) {
          margin-top: 21px;
        }
      }
    }

    .subheadline {
      font-size: 21px;
      margin: 0;
      text-align: right;
    }

    .square {
      background-color: var(--persian-red);
      color: transparent;
      display: inline-block;
      height: 8px;
      margin-left: 3px;
      width: 8px;

      @media screen and (min-width: 768px) {
        height: 21px;
        margin-left: 0;
        width: 21px;
      }
    }
  }
</style>

<div class="container">
  <div class="headlines">
    <h2 class="headline hello">
      Hello
      <span class="square">.</span>
    </h2>
    <h2 class="headline">{whoAmI}</h2>
    <h3 class="subheadline">{jobTitle}</h3>
  </div>
</div>
