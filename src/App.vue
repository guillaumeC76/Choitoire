<template>
  <div id="app">
    <Header></Header>
    <Home></Home>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Home from './components/Home.vue';

export default {
  name: 'App',
  components: {
    Header,
    Home,
  },
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Langar&display=swap');

html, body {
  height: 100%;
  margin: 0;
  font-family: 'Langar', cursive;
}

#app {
  height: 100%;
}
</style>
