<template>
  <div id="footer">
    <div id="footer-up">
      <div class="container"></div>
    </div>
    <div id="footer-down">
      <div class="container">
        <a href="#" class="btn"> Sign-up now!</a>
        <div>
          <span>follow us!</span>
          <ul>
            <li v-for="img in social" :key="img">
              <a href="#">
                <img :src="`/img/${img}`" alt="social icon" />
              </a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FooterApp',
  data: () => ({
    social: [
      'footer-facebook.png',
      'footer-twitter.png',
      'footer-youtube.png',
      'footer-pinterest.png',
      'footer-periscope.png',
    ],
  }),
};
</script>

<style lang="scss" scoped>
@import '@/assets/scss/custom.scss';

#footer-up {
  background-image: url('@/assets/img/footer-bg.jpg');
}

#footer-down {
  background-color: rgb(48, 48, 48);

  padding: 2.5rem 0;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;

    & > div {
      display: flex;
      column-gap: 2rem;
      align-items: center;

      span {
        color: $dc-blue;
        font-size: 1.2rem;
        text-transform: uppercase;
        font-weight: bold;
      }

      ul {
        display: flex;
        column-gap: 0.5rem;

        li {
          list-style-type: none;
        }
      }
    }

    .btn {
      padding: 1rem;
      border: $dc-blue solid 3px;

      color: white;
      text-transform: uppercase;
      text-decoration: none;
      font-weight: bold;
    }
  }
}
</style>
