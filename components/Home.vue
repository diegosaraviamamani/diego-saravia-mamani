<template>
  <v-img
    src="/diego-saravia-mamani/laptop.jpg"
    min-height="100vh"
    gradient="to top right, rgba(0,0,0,.5), rgba(0,0,0,.5)"
  >
    <v-container id="index" fill-height>
      <v-row justify="center">
        <v-col cols="10">
          <v-card color="transparent" class="white--text" flat>
            <v-card-title class="mt-10 mt-sm-0">
              <v-row>
                <v-col cols="12">
                  <h1 class="font-weight-regular text-left display-3 text">Diego Saravia Mamani</h1>
                </v-col>
                <v-col cols="12">
                  <div class="headline text-uppercase text-left text">Front End Developer Junior</div>
                  <div
                    class="subtitle-1 text-left font-italic text"
                  >- Vue.js, Vuetify, Vuex, Nuxt, Quasar, HTML, CSS, React, Redux</div>
                </v-col>
              </v-row>
            </v-card-title>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-img>
</template>

<script>
export default {
  data() {
    return {
      screenWidth: screen.width
    }
  },
  computed: {
    style() {
      return this.data
    }
  }
}
</script>

<style lang="scss" scoped>
.headline {
  letter-spacing: 7px !important;
}
</style>