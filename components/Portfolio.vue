<template>
  <v-img min-height="100vh">
    <v-container id="portfolio" grey lighten-2 fluid fill-height grid-list-xl cols="10">
      <v-container>
        <v-row class="my-12 mx-xl-12" justify="center" dense>
          <v-col cols="12" class="text-center my-12">
            <span class="display-2 text">PORTAFOLIO</span>
          </v-col>
          <v-col cols="12" sm="6" md="5" lg="4" class="pa-4">
            <v-hover v-slot:default="{hover}">
              <v-card :elevation="hover ? 12 : 2" class="project" :class="{'on-hover': hover}">
                <v-img
                  src="/diego-saravia-mamani/huddle-landing-page.png"
                  :aspect-ratio="16/9"
                  @click="vamos('https://diegoxd93.github.io/huddle-landing-page/')"
                  class=".v-img"
                >
                  <v-scale-transition origin="center">
                    <div
                      class="black darken-4 transition-fast-in-fast-out v-card--reveal fill-height"
                      v-if="hover"
                    >
                      <v-card-title class="title white--text">
                        <v-row class="fill-height flex-column" justify="space-between">
                          <p class="subheading text-center text-uppercase">Huddle Landing Page</p>
                          <p class="body-1 text-center">Front-end Mentor Challenge</p>
                          <div class="row justify-center">
                            <v-chip color="error" small class="mx-1">HTML</v-chip>
                            <v-chip color="primary" small class="mx-1">CSS</v-chip>
                          </div>
                          <div>
                            <v-icon>book</v-icon>
                          </div>
                        </v-row>
                      </v-card-title>
                    </div>
                  </v-scale-transition>
                </v-img>
              </v-card>
            </v-hover>
          </v-col>
          <v-col cols="12" sm="6" md="5" lg="4" class="pa-4">
            <v-hover v-slot:default="{hover}">
              <v-card :elevation="hover ? 12 : 2" class="project" :class="{'on-hover': hover}">
                <v-img
                  src="/diego-saravia-mamani/four-card-feature-section-master.png"
                  :aspect-ratio="16/9"
                  @click="vamos('https://diegoxd93.github.io/four-card-feature-section-master/')"
                  class=".v-img"
                >
                  <v-scale-transition origin="center">
                    <div
                      class="black darken-4 transition-fast-in-fast-out v-card--reveal fill-height"
                      v-if="hover"
                    >
                      <v-card-title class="title white--text">
                        <v-row class="fill-height flex-column" justify="space-between">
                          <p
                            class="subheading text-center text-uppercase wrap"
                          >Four Card Feature Section</p>
                          <p class="body-1 text-center">Front-end Mentor Challenge</p>
                          <div class="row justify-center">
                            <v-chip color="error" small class="mx-1">HTML</v-chip>
                            <v-chip color="primary" small class="mx-1">CSS</v-chip>
                          </div>
                          <div>
                            <v-icon>book</v-icon>
                          </div>
                        </v-row>
                      </v-card-title>
                    </div>
                  </v-scale-transition>
                </v-img>
              </v-card>
            </v-hover>
          </v-col>
          <v-col cols="12" sm="6" md="5" lg="4" v-for="n in 3" :key="n.id" class="pa-4">
            <v-hover v-slot:default="{hover}">
              <v-card :elevation="hover ? 12 : 2" class="project" :class="{'on-hover': hover}">
                <v-img
                  src="/diego-saravia-mamani/laptop.jpg"
                  :aspect-ratio="16/9"
                  @click="alert"
                  class=".v-img"
                >
                  <v-scale-transition origin="center">
                    <div
                      class="black darken-4 transition-fast-in-fast-out v-card--reveal fill-height"
                      v-if="hover"
                    >
                      <v-card-title class="title white--text">
                        <v-row class="fill-height flex-column" justify="space-between">
                          <p class="subheading text-center text-uppercase">Titulo</p>
                          <p class="body-1 text-center">Front-end Mentor Challenge</p>
                          <div class="row justify-center">
                            <v-chip color="success" small class="mx-1">Vuejs</v-chip>
                            <v-chip color="primary" small class="mx-1">Vuetify</v-chip>
                          </div>
                          <div>
                            <v-icon>book</v-icon>
                          </div>
                        </v-row>
                      </v-card-title>
                    </div>
                  </v-scale-transition>
                </v-img>
              </v-card>
            </v-hover>
          </v-col>
        </v-row>
      </v-container>
    </v-container>
  </v-img>
</template>

<script>
export default {
  methods: {
    alert() {
      alert('hola')
    },
    vamos(url) {
      location.href = url
    }
  }
}
</script>

<style lang="scss" scoped>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.8;
  position: absolute;
  width: 100%;
  &:hover {
    cursor: pointer;
  }
}

.text {
  position: relative;
  &::after {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    right: 0;
    margin: auto;
    width: 70%;
    height: 2px;
    background: #212121;
    border-radius: 1px;
  }
}
</style>