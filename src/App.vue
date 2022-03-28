<template>
  <div id="app">
    <header>
      <NavBar />
    </header>
    <main>
      <MainContent />
      <MainMenu />
    </main>

    <footer>
      <FooterApp />
    </footer>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue';
import MainContent from '@/components/MainContent.vue';
import MainMenu from './components/MainMenu.vue';
import FooterApp from './components/FooterApp.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    MainContent,
    MainMenu,
    FooterApp,
  },
};
</script>

<style lang="scss">
@import '@/assets/scss/custom.scss';

#app {
  width: 99vw;
}

.dark {
  background-color: black;
  color: white;
}

.blue {
  background-color: $dc-blue;
}
</style>
