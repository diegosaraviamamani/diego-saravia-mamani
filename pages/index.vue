<template>
  <v-app>
    <Hero />
    <v-img
      src="/diego-saravia-mamani/laptop.jpg"
      max-height="100vh"
      gradient="to top right, rgba(0,0,0,.5), rgba(0,0,0,.5)"
    >
      <v-container id="index" wrap fill-height>
        <v-row justify="center">
          <v-col cols="10">
            <v-card color="transparent" class="white--text" flat>
              <v-card-title class="mt-10 mt-sm-0">
                <v-row>
                  <v-col cols="12">
                    <h1 class="display-3 font-weight-regular text-left">Diego Saravia Mamani</h1>
                  </v-col>
                  <v-col cols="12">
                    <div class="headline text-uppercase text-left">Front End Developer Junior</div>
                    <div
                      class="subtitle-1 text-left font-italic"
                    >- Vue.js, Vuetify, Vuex, Nuxt, Quasar, HTML, CSS, React, Redux</div>
                  </v-col>
                </v-row>
              </v-card-title>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-img>

    <v-container id="about" wrap>
      <h1 v-for="n in 20" :key="n.id">{{ n }}</h1>
      <h1>asdasd</h1>
    </v-container>

    <v-footer>
      <div>
        <span>&copy; {{ new Date().getFullYear() }}</span>
      </div>
      <div>
        <p>footer</p>
      </div>
    </v-footer>
  </v-app>
</template>

<script>
import Hero from '~/components/Hero'
export default {
  components: {
    Hero
  }
}
</script>
<style lang="scss" scoped>
.headline {
  letter-spacing: 7px !important;
}
</style>
