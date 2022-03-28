<template>
  <div id="app">
    <div class="container">
      <header>
        <NavBar />
      </header>

      <main></main>
    </div>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar.vue';

export default {
  name: 'App',
  components: {
    NavBar,
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
</style>
