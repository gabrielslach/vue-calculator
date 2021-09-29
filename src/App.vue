<template>
  <div>
    <Screen :input="this.input" />
    <Buttons @input-append="inputAppend" />
  </div>
</template>

<script>
import Screen from './components/Screen';
import Buttons from './components/Buttons';

export default {
  name: 'App',
  components: {
    Screen,
    Buttons
  },
  data() {
    return {
      input: ''
      }
  },
  methods: {
    inputAppend(character) {
      this.input+= character;
    }
  }
}
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
