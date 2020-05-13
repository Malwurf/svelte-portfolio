<script>
  const whoAmI = "I'm Przemek";
  const jobTitle = "< Frontend developer />";
</script>

<style lang="scss">
  .container {
    align-items: center;
    display: flex;
    height: 100%;
    justify-content: center;
    width: 89vw;

    .headline {
      font-size: 130px;
      margin: 0;

      &.hello {
        align-items: flex-end;
        display: flex;
        line-height: 90px;
      }

      & + .headline {
        margin-top: 21px;
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
      height: 20px;
      width: 20px;
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
