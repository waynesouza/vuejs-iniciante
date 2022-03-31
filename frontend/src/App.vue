<template>
  <div>
    <Navbar :logo="logo_src" :alt="app_name"/>
    <div>
      <router-view/>
    </div>
    <Footer/>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";
import Footer from "@/components/Footer";

export default {
  components: {
    Navbar,
    Footer
  },
  data() {
    return {
      logo_src: '/img/logo.png',
      app_name: 'Make Your Burger'
    }
  }
}
</script>

<style>
  * {
    font-family: Helvetica;
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  .main-container {
    margin: 50px; /* Ajustar o conteúdo e dar mais espaçamento em todos os cantos */
    min-height: 250px; /* Ganha um "corpo" a mais, o conteúdo do site */
  }

  h1 {
    text-align: center;
    font-size: 42px;
    margin-bottom: 30px;
    color: #222;
  }

  :root .p-dropdown-panel .p-dropdown-items .p-dropdown-item.p-highlight {
    color: #ffffff !important;
    background: #808080 !important;
  }

  .error-msg {
    color: #ff0000;
    font-size: small;
    margin-top: 6px;
    padding-left: 12px;
  }
</style>
