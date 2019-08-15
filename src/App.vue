<template>
  <v-app>
    <div class="application--wrap">
      <aside class="aside text-xs-center v-navigation-drawer--fixed v-navigation-drawer--open">
        <div class="layout align-center column fill-height justify-center">
          <img :src="img(content.logo)" alt="logo" height="160px" />
          <div class="display-1 mt-2 white--text">Desarrollo</div>
          <span class="title font-weight-light white--text mb-5">de productos digitales</span>
          <div>
            <button
              type="button"
              class="text-capitalize subheading font-weight-light mb-3 v-btn v-btn--flat theme--dark"
            >
              <div class="v-btn__content">
                <span>Nosotros</span>
              </div>
            </button>
          </div>
          <div>
            <button
              type="button"
              class="text-capitalize subheading font-weight-light mb-3 v-btn v-btn--flat theme--dark"
            >
              <div class="v-btn__content">
                <span>Servicios</span>
              </div>
            </button>
          </div>

          <div>
            <button
              type="button"
              class="text-capitalize subheading font-weight-light mb-3 v-btn v-btn--flat theme--dark"
            >
              <div class="v-btn__content">
                <span>Portafolio</span>
              </div>
            </button>
          </div>

          <div>
            <button
              type="button"
              class="text-capitalize subheading font-weight-light mb-3 v-btn v-btn--flat theme--dark"
            >
              <div class="v-btn__content">
                <span>Contacto</span>
              </div>
            </button>
          </div>
          <!--<div class="mt-auto">
          <div class="my-4">
            <a href="https://twitter.com/john" title="Twitter profile" class="mx-2">
              <i aria-hidden="true" class="v-icon mdi mdi-twitter-box theme--dark"></i>
            </a>
            <a
              data-v-4d8f3726
              href="https://linkedin.com/john"
              title="LinkedIn profile"
              class="mx-2"
            >
              <i data-v-4d8f3726 aria-hidden="true" class="v-icon mdi mdi-linkedin-box theme--dark"></i>
            </a>
            <a data-v-4d8f3726 href="https://github.com/john" title="Github profile" class="mx-2">
              <i data-v-4d8f3726 aria-hidden="true" class="v-icon mdi mdi-github-box theme--dark"></i>
            </a>
          </div>
          </div>-->
        </div>
        <div class="v-navigation-drawer__border"></div>
      </aside>
      <!--<v-app-bar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Vuetify</span>
        <span class="font-weight-light">MATERIAL DESIGN</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>open_in_new</v-icon>
      </v-btn>
      </v-app-bar>-->

      <v-content>
        <router-view />
      </v-content>
    </div>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    logo: "logo2.svg"
  }),
  methods: {
    img(img) {
      return require(`@/assets/${img}`);
    }
  },
  computed: {
    content() {
      return {
        logo: "favicon2.svg"
      };
    }
  }
};
</script>
<style>
.aside {
  height: 100%;
  margin-top: 0px;
  max-height: calc(100% - 0px);
  transform: translateX(0px);
  width: 300px;
  background-color: black;
}
.application--wrap {
  flex: 1 1 auto;
  backface-visibility: hidden;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  max-width: 100%;
  position: relative;
}
.v-btn {
  padding: 0 16px;
  align-items: center;
  border-radius: 2px;
  display: inline-flex;
  height: 36px;
  flex: 0 0 auto;
  font-size: 14px;
  font-weight: 500;
  justify-content: center;
  margin: 6px 8px;
  min-width: 88px;
  outline: 0;
  text-transform: uppercase;
  text-decoration: none;
  transition: 0.3s cubic-bezier(0.25, 0.8, 0.5, 1), color 1ms;
  position: relative;
  vertical-align: middle;
  user-select: none;
}
</style>
