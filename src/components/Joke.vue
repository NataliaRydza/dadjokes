<template>
  <div class="container">
    <div class="joke">
      <div class="joke__body">
        <img class="joke__user" v-bind:src="'assets/img/' + img + '.png'" />
        <p class="joke__text">{{joke}}</p>
      </div>
      <div class="joke__likes">
        <button id="btn-up" class="btn-like btn-like--up" @click="likesUp"></button>
        <span id="likes-up" class="likes-count likes-count--up">{{plusLike}}</span>
        <button id="btn-down" class="btn-like btn-like--down" @click="likesDown"></button>
        <span id="likes-down" class="likes-count likes-count--down">{{minusLike}}</span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Joke",
  props: ["img", "joke", "upLikesProp", "downLikesProp"],
  data() {
    return {
      plusLike: this.upLikesProp,
      minusLike: this.downLikesProp
    };
  },
  methods: {
    likesUp() {
      return this.plusLike++;
    },
    likesDown() {
      return this.minusLike++;
    }
  }
};
</script>
<style>
</style>