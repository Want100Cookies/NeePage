<template>
  <div id="app">
    <Translate text="Nee" lang="en"/>
  </div>
</template>

<script>
import Translate from './components/Translate.vue';

export default {
  name: 'app',
  components: {
    Translate,
  },
  mounted() {
    console.log(Translate.langs);
  },
};
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
