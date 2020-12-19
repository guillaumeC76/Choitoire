<template>
  <div class="header_page">
      <div class="menu_header">
        <div class="option_menu">Accueil</div>
        <div class="option_menu">Mes histoires</div>
        <div class="option_menu">Qui suis-je ?</div>
        <div class="option_menu">Contact</div>
      </div>
      <div class="bottom-header"></div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header_page {
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
}
</style>
