<template>
  <div class="bg-white">
    <div class="container">
      <div class="header">
        <img src="@/assets/img/dc-logo.png" alt="DC Logo" />

        <nav>
          <ul>
            <li v-for="(link, index) in navItems" :key="index" :class="{ active: link.active }">
              <a :href="link.url" @click="changeActive(index)">{{ link.text }}</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  data: () => ({
    navItems: [
      {
        text: 'Characters',
        url: '#',
        active: true,
      },
      {
        text: 'comics',
        url: '#',
        active: false,
      },
      {
        text: 'movies',
        url: '#',
        active: false,
      },
      {
        text: 'tv',
        url: '#',
        active: false,
      },
      {
        text: 'games',
        url: '#',
        active: false,
      },
      {
        text: 'collectibles',
        url: '#',
        active: false,
      },
      {
        text: 'videos',
        url: '#',
        active: false,
      },
      {
        text: 'fans',
        url: '#',
        active: false,
      },
      {
        text: 'news',
        url: '#',
        active: false,
      },
      {
        text: 'shop',
        url: '#',
        active: false,
      },
    ],
  }),
  methods: {
    changeActive(newIndex) {
      this.navItems.forEach((item, index) => {
        if (index === newIndex) this.navItems[index].active = true;
        else this.navItems[index].active = false;
      });
    },
  },
};
</script>

<style lang="scss" scoped>
@import '@/assets/scss/custom.scss';
.header {
  height: 7rem;
  padding-top: 0.5rem;

  display: flex;
  justify-content: space-between;
  align-items: center;

  img {
    height: 5rem;
  }

  nav {
    height: 100%;
    ul {
      display: flex;
      justify-content: end;
      height: 100%;

      li {
        list-style-type: none;
        text-transform: uppercase;

        font-size: 0.8rem;
        font-weight: 600;

        height: 100%;
        padding: 0 0.5rem;
        display: flex;
        align-items: center;

        border-bottom: 5px solid transparent;

        a {
          text-decoration: none;
          color: black;
        }

        &.active,
        &:active {
          border-color: $dc-blue;

          a {
            color: $dc-blue;
          }
        }
      }
    }
  }
}
</style>
