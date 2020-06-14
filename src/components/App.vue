<template>
  <div>
    <Joke
      v-for="(joke, index) in jokes"
      v-bind:img="joke.img"
      v-bind:joke="joke.joke"
      v-bind:upLikesProp="joke.upLikes"
      v-bind:downLikesProp="joke.downLikes"
      v-bind:key="index"
    />
  </div>
</template>

<script>
import Joke from "./Joke.vue";
export default {
  name: "App",
  components: {
    Joke: Joke
  },
  data() {
    return {
      jokes: [
        {
          img: "user01",
          joke: `The secret service isn't allowed to yell "Get down!" anymore when the president is about to be attacked. Now they have to yell "Donald, duck!`,
          upLikes: 13,
          downLikes: 24
        },

        {
          img: "user02",
          joke: `Why did the invisible man turn down the job offer? He couldn't see himself doing it.`,
          upLikes: 50,
          downLikes: 10
        },

        {
          img: "user03",
          joke: `I bought some shoes from a drug dealer. I don't know what he laced them with, but I was tripping all day!`,
          upLikes: 30,
          downLikes: 2
        },

        {
          img: "user04",
          joke: `Did you hear the news? FedEx and UPS are merging. They’re going to go by the name Fed-Up from now on.`,
          upLikes: 15,
          downLikes: 8
        },

        {
          img: "user05",
          joke: `My daughter screeched, "Daaaaaad, you haven't listened to one word I've said, have you!?" What a strange way to start a conversation with me...`,

          upLikes: 90,
          downLikes: 44
        },

        {
          img: "user06",

          joke: `My wife tried to unlatch our daughter's car seat with one hand and said, "How do one armed mothers do it?" Without missing a beat I replied, "Single handedly."`,

          upLikes: 38,
          downLikes: 1
        },

        {
          img: "user07",
          joke: `When a dad drives past a graveyard: Did you know that's a popular cemetery? Yep, people are just dying to get in there!`,
          upLikes: 66,
          downLikes: 35
        },

        {
          img: "user08",
          joke: `My friend keeps saying "cheer up man it could be worse, you could be stuck underground in a hole full of water." I know he means well.`,
          upLikes: 27,
          downLikes: 18
        },

        {
          img: "user09",
          joke: `The fattest knight at King Arthur’s round table was Sir Cumference. He acquired his size from too much pi.`,
          upLikes: 42,
          downLikes: 9
        }
      ]
    };
  }
};
</script>
  <style>
</style>