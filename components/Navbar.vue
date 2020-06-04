<template>
  <div>
    <v-app-bar fixed dark :color="color" scroll-off-screen :flat="flat" border="bottom">
      <v-container>
        <v-row>
          <template v-slot:img="{props}">
            <v-img v-bind="props"></v-img>
          </template>
          <v-img contain :src="logo" max-width="120" />
          <v-spacer></v-spacer>
          <v-toolbar-items class="d-none d-md-inline">
            <v-btn
              text
              class="link text"
              v-for="link in links"
              :key="link.id"
              :href="link.href"
              exact
            >{{ link.text }}</v-btn>
          </v-toolbar-items>
          <v-app-bar-nav-icon class="d-inline d-md-none" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
        </v-row>
      </v-container>
    </v-app-bar>
    <v-navigation-drawer fixed class="d-md-none" v-model="drawer" temporary right>
      <v-list>
        <v-list-item v-for="link in links" :key="link.id" link :href="link.href" exact>
          <v-list-item-content>
            <v-list-item-title>{{link.text}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
// alert(
//   'La resolución de pantalla que tienes en este momento es de: ' +
//     screen.width +
//     ' x ' +
//     screen.height
// )
export default {
  data: () => {
    return {
      links: [
        { text: 'Inicio', href: '#index' },
        { text: 'Sobre mi', href: '#about' },
        { text: 'Portafolio', href: '#portfolio' },
        { text: 'Contactame', href: '#contact' }
      ],
      scrollPosition: null,
      scrollDefault: 100,
      color: 'transparent',
      logo: '/diego-saravia-mamani/logo-dark.png',
      flat: true,
      drawer: null
    }
  },
  watch: {
    scrollPosition(newValue) {
      if (this.scrollPosition < this.scrollDefault) {
        this.color = 'transparent'
        this.flat = true
      } else {
        this.color = '#1D2029'
        this.flat = false
      }
    }
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll)
  },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY
    }
  }
}
</script>

<style lang="scss" scoped>
.link {
  font-family: 'Quicksand', 'Roboto', sans-serif !important;
  text-decoration: none;
  color: white;
}
</style>