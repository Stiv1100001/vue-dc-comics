<template>
  <div id="footer">
    <div id="footer-up">
      <div class="container">
        <div class="url-container">
          <ul v-for="(link, index) in links" :key="index">
            <li v-for="(url, index2) in link" :key="index2">
              <a href="#"> {{ url }}</a>
            </li>
          </ul>
        </div>
        <img src="@/assets/img/dc-logo-bg.png" alt="" />
      </div>
    </div>
    <div id="footer-down">
      <div class="container">
        <a href="#" class="btn"> Sign-up now!</a>
        <div>
          <span>follow us!</span>
          <ul>
            <li v-for="(img, index) in social" :key="index">
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

    links: [
      [
        'DC COMICS',
        'characters',
        'characters',
        'characters',
        'characters',
        'characters',
        'characters',
        'characters',
      ],
      ['SHOP', 'characters', 'characters'],
      [
        'DC',
        'characters',
        'characters',
        'characters',
        'characters',
        'characters',
        'characters',
        'characters',
        'characters',
        'characters',
        'characters',
        'characters',
      ],
      ['SITES', 'characters', 'characters', 'characters', 'characters', 'characters'],
    ],
  }),
};
</script>

<style lang="scss" scoped>
@import '@/assets/scss/custom.scss';

#footer-up {
  background-image: url('@/assets/img/footer-bg.jpg');
  background-size: cover;

  .container {
    position: relative;
    overflow: hidden;

    img {
      height: 50vh;
      position: absolute;
      top: -50px;
      right: 50px;
    }
  }

  .url-container {
    max-width: 45%;
    max-height: 40vh;
    padding: 3rem 0;

    display: flex;
    flex-direction: column;
    flex-wrap: wrap;

    ul {
      margin-bottom: 1.5rem;
      li {
        list-style-type: none;
        font-size: 0.8rem;

        &:first-child {
          font-size: 1.1rem;
          margin-bottom: 1rem;
          a {
            color: white;
          }
        }

        a {
          color: gray;
          text-decoration: none;
        }
      }
    }
  }
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
