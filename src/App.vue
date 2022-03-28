<template>
  <div id="app">
    <header class="container">
      <NavBar />
    </header>
    <main class="dark">
      <div class="container">
        <MainContent />
      </div>
    </main>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue';
import MainContent from '@/components/MainContent.vue';

export default {
  name: 'App',
  components: {
    NavBar,
    MainContent,
  },
};
</script>

<style lang="scss">
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  font-family: sans-serif;
}

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
</style>
