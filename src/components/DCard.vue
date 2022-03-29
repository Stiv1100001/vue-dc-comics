<template>
  <div id="card">
    <img :src="comic.thumb" :alt="comic.series" />
    <h3>{{ comic.series }}</h3>
  </div>
</template>

<script>
export default {
  name: 'DCards',
  props: {
    comic: Object,
  },
};
</script>

<style lang="scss" scoped>
#card {
  width: calc(100% / 6 - 1rem);
  margin-right: 1rem;

  margin-bottom: 3rem;

  img {
    width: 100%;
    height: 12rem;
    margin-bottom: 1rem;
    object-fit: cover;
    object-position: 0px 0px;
  }

  h3 {
    font-weight: 200;
  }
}
</style>
