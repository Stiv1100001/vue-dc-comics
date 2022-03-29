<template>
  <div class="bg-black">
    <div id="jumbotron"></div>
    <div class="container">
      <h1 class="title">Current Series</h1>
      <div class="cards">
        <DCard v-for="(comic, index) in comics" :key="index" :comic="comic" />
      </div>
      <div class="buttons">
        <button class="btn">Load MOre</button>
      </div>
    </div>
  </div>
</template>

<script>
import comics from '@/assets/dc-comics.json';
import DCard from './DCard.vue';

export default {
  name: 'MainContent',
  data: () => ({
    comics,
  }),
  components: { DCard },
  methods: {
    async fetchComics() {
      await fetch('/dc-comics.json').then((res) => {
        this.comics = res.json();
      });
    },
  },
};
</script>

<style lang="scss" scoped>
@import '@/assets/scss/custom.scss';

.content {
  padding: 5rem 0;
}

#jumbotron {
  height: 40vh;

  background-image: url('@/assets/img/jumbotron.jpg');
  background-size: cover;
}

.container {
  position: relative;
  padding: 3rem 0;

  .title {
    font-size: 1.7rem;
    text-transform: uppercase;
    background-color: $dc-blue;
    width: fit-content;
    padding: 0.7rem;

    position: absolute;
    left: 0;
    top: 0;

    transform: translateY(-50%);
  }

  .cards {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }

  .buttons {
    display: flex;
    justify-content: center;

    .btn {
      background-color: $dc-blue;
      color: white;

      border: none;

      text-transform: uppercase;
      font-size: 1rem;
      font-weight: bold;

      padding: 0.5rem 3rem;
    }
  }
}
</style>
