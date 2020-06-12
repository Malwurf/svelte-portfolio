<script>
  import {
    ballIcon,
    worldIcon,
    directionIcon,
    avengersIcon,
    tvIcon,
    eatingIcon,
    familyIcon,
    remoteIcon
  } from "../../icons/Icons.svelte";
</script>

<style lang="scss">
  .about-list {
    align-items: center;
    display: flex;
    flex-direction: column;
    flex-wrap: wrap;
    justify-content: space-between;
    list-style: none;
    max-width: 987px;
    padding-left: 0;

    @media screen and (min-width: 1024px) {
      flex-direction: row;
    }

    .item {
      align-items: center;
      display: flex;
      justify-content: flex-start;
      margin-bottom: 21px;
      width: 89%;

      @media screen and (min-width: 1024px) {
        width: 50%;
      }
    }

    .text {
      font-size: 13px;

      @media screen and (min-width: 640px) {
        font-size: 21px;
      }
    }

    .icon {
      border-right: 2px solid var(--pegasus-red);
      display: block;
      height: 100%;
      margin-right: 20px;
      max-height: 34px;
      max-width: 34px;
      padding-bottom: 8px;
      padding-right: 13px;
      padding-top: 8px;
      position: relative;
      width: 100%;

      @media screen and (min-width: 640px) {
        max-height: 55px;
        max-width: 55px;
        padding: 13px 21px;
      }
    }
  }

  .headline {
    &.red {
      color: var(--pegasus-red);
      margin: 0;
    }

    &.blue {
      color: var(--just-blue);
      font-size: 13px;
      margin-bottom: 13px;
      margin-top: 0;

      @media screen and (min-width: 640px) {
        font-size: 21px;
      }
    }

    &.quotation {
      font-size: 21px;
      font-style: italic;
      font-weight: lighter;
    }

    &.main {
      font-size: 21px;
      margin: 0;

      @media screen and (min-width: 640px) {
        font-size: 34px;
      }
    }
  }
</style>

<h1 class="page-headline">About me in a pill</h1>

<div class="container">
  <h2 class="blue headline target">Frontend Developer</h2>
  <h1 class="main headline">Przemysław Korościk</h1>

  <ul class="about-list">
    <li class="item target">
      <span class="icon">
        {@html worldIcon}
      </span>
      <p class="text">
        I live in small village (Wilczyce) near Wrocław in Poland.
      </p>
    </li>
    <li class="item target">
      <span class="icon">
        {@html directionIcon}
      </span>
      <p class="text">
        I am self-taught. I chose frontend because I like to see the results of
        my job instantly.
      </p>
    </li>
    <li class="item target">
      <span class="icon">
        {@html familyIcon}
      </span>
      <p class="text">
        I have a beautiful wife and daughter as well as several friends which I
        like spending time with them playing board games or eat.
      </p>
    </li>
    <li class="item target">
      <span class="icon">
        {@html ballIcon}
      </span>
      <p class="text">
        Yup. I love to play & watch football. Of course, I support Juventus from
        Turin.
      </p>
    </li>
    <li class="item target">
      <span class="icon">
        {@html avengersIcon}
      </span>
      <p class="text">
        In my free time, I like to watch sci-fi movies and TV series. Best ever
        is Avengers and Westworld of course.
      </p>
    </li>
    <li class="item target">
      <span class="icon">
        {@html eatingIcon}
      </span>
      <p class="text">
        I like Italian food. Sometimes I cook dinners myself. I love meat... and
        cheese... and pizza... and ketchup... ;)
      </p>
    </li>
    <li class="item target">
      <span class="icon">
        {@html remoteIcon}
      </span>
      <p class="text">
        I'm only interested in remote work job offers. If you have some just
        send me an offer including salary range :)
      </p>
    </li>
  </ul>

  <h2 class="red headline quotation">"Love You 3000"</h2>
</div>
