<template>
  <div id="app">
    <FormGenerator
            :data="objectToConvert"
    />
  </div>
</template>

<script>
  import FormGenerator from './components/FormGenerator';

  export default {
    name: 'app',

    components: {
      FormGenerator,
    },

    data () {
      return {
        objectToConvert: window.prebidConfig,
      }
    }
  }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
