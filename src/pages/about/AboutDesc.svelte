<script context="module">
  import {
    ballIcon,
    worldIcon,
    directionIcon,
    avengersIcon,
    eatingIcon,
    familyIcon,
    remoteIcon,
  } from "../../icons/Icons.svelte";

  export const aboutMe = [
    {
      description: "I live in small village (Wilczyce) near Wrocław in Poland.",
      icon: worldIcon,
    },
    {
      description:
        "I am self-taught. I chose frontend because I like to see the results of my job instantly.",
      icon: directionIcon,
    },
    {
      description:
        "I have a beautiful wife and daughter as well as several friends which I like spending time with them playing board games or eat.",
      icon: familyIcon,
    },
    {
      description:
        "Yup. I love to play & watch football. Of course, I support Juventus from Turin.",
      icon: ballIcon,
    },
    {
      description:
        "In my free time, I like to watch sci-fi movies and TV series. Best ever is Avengers and Westworld of course.",
      icon: avengersIcon,
    },
    {
      description:
        "I like Italian food. Sometimes I cook dinners myself. I love meat... and cheese... and pizza... and ketchup... ;)",
      icon: eatingIcon,
    },
    {
      description:
        "I'm only interested in remote work job offers. If you have some just send me an offer including salary range :)",
      icon: remoteIcon,
    },
  ];
</script>
