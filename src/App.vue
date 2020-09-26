<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <joke-button> </joke-button>
    <div></div>
    <loud-joke v-if="jokeType === 'loud'" key="loud" > </loud-joke>
    <snake-joke v-else-if="jokeType === 'snake'" key="snake"> </snake-joke>
    <normal-joke v-else-if="jokeType === 'normal'" key="normal"> </normal-joke>
  </div>
</template>

<script>
import JokeButton from './components/jokeButton.vue'
import LoudJoke from './components/loudjoke.vue'
import SnakeJoke from './components/snakeJoke.vue'
import NormalJoke from './components/normalJoke.vue'


export default {
  name: "App",
  components: {
    JokeButton,
    LoudJoke,
    SnakeJoke,
    NormalJoke

  },
  computed: {
    jokeType: function() {
      return this.$store.state.jokeType
    }
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
