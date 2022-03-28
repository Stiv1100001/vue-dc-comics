<template>
  <div id="main-menu">
    <ul>
      <li v-for="(link, index) in menuLinks" :key="index">
        <img :src="`../img/${link.img}`" :alt="link.text" />
        <span>{{ link.text }}</span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'MainMenu',
  data: () => ({
    menuLinks: [
      {
        text: 'Digital Comics',
        img: 'buy-comics-digital-comics.png',
      },
      {
        text: 'DC merchandising',
        img: 'buy-comics-merchandise.png',
      },
      {
        text: 'subscription',
        img: 'buy-comics-subscriptions.png',
      },
      {
        text: 'comic shop locator',
        img: 'buy-comics-shop-locator.png',
      },
      {
        text: 'dc power visa',
        img: 'buy-dc-power-visa.svg',
      },
    ],
  }),
};
</script>

<style lang="scss" scoped>
#main-menu {
  padding: 3rem 0;

  ul {
    display: flex;
    justify-content: space-around;

    color: white;

    li {
      list-style-type: none;

      display: flex;
      align-items: center;
      column-gap: 0.5rem;

      img {
        height: 3.5rem;
        max-width: 3.5rem;
      }

      span {
        font-size: 0.9rem;
        font-weight: 300;
        text-transform: uppercase;
      }
    }
  }
}
</style>
