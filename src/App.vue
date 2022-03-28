<template>
  <div id="app">
    <header class="container">
      <NavBar />
    </header>
    <main>
      <div class="dark">
        <div class="container">
          <MainContent />
        </div>
      </div>
      <div class="blue">
        <div class="container">
          <MainMenu />
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue';
import MainContent from '@/components/MainContent.vue';
import MainMenu from './components/MainMenu.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    MainContent,
    MainMenu,
  },
};
</script>

<style lang="scss">
@import '@/assets/scss/custom.scss';

#app {
  width: 100vw;
}

.container {
  max-width: 80%;
  margin: 0 auto;
}

.dark {
  background-color: black;
  color: white;
}

.blue {
  background-color: $dc-blue;
}
</style>
