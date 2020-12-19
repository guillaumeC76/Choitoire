<template>
  <div id="app">
    <div class="menu_header">
      <div class="option_menu" @click="mettreAccueil()">Accueil</div>
      <div class="option_menu" @click="enleverAccueil()">Mes histoires</div>
      <div class="option_menu">Qui suis-je ?</div>
      <div class="option_menu">Contact</div>
    </div>
    <div class="bottom-header"></div>
    <Home v-if="accueil"></Home>
  </div>
</template>

<script>
import Home from './components/Home.vue';

export default {
  name: 'App',
  components: {
    Home,
  },
  data() {
    return {
      accueil: true,
    };
  },
  methods: {
    enleverAccueil() {
      this.accueil = false;
    },
    mettreAccueil() {
      this.accueil = true;
    },
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

.menu_header {
    width: 100%;
    height: 100px;
    background-color: #181828;
    display: flex;
    align-items: center;
    justify-content: space-around;

    .option_menu {
        color: white;
        font-size: 2em;
        background: linear-gradient(90deg, red, orange, yellow, green);
        background-clip: text;
        -webkit-background-clip: text;
        transition: 0.5s;
    }

    .option_menu:hover {
        cursor: pointer;
        color: transparent;
        transition: 0.5s;
    }
}

    .bottom-header::before {
        background-image: url(https://1.bp.blogspot.com/-gxsOcYWghHA/Xp_izTh4sFI/AAAAAAAAU8s/y637Fwg99qAuzW9na_NT_uApny8Vce95gCEwYBhgL/s1600/header-footer-gradient-bg.png);
    }

    .bottom-header::before {
        content: "";
        display: block;
        width: 100%;
        height: 4px;
        background-repeat: repeat-x;
        background-size: contain;
        position: absolute;
        top: 100px;
        left: 0;
        opacity: 0.5;
    }
</style>
