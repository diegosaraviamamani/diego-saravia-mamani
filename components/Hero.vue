<template>
  <div>
    <v-app-bar menup fixed dark :color="color" scroll-off-screen fade-img-on-scroll :flat="flat">
      <v-container>
        <v-row>
          <template v-slot:img="{props}">
            <v-img v-bind="props"></v-img>
          </template>
          <v-img contain :src="logo" max-width="120" />
          <v-spacer></v-spacer>
          <v-toolbar-items class="d-none d-md-inline">
            <v-btn
              v-for="link in links"
              :key="link.id"
              :class="textColor"
              text
              flat
              :href="link.href"
            >{{ link.text }}</v-btn>
          </v-toolbar-items>
          <v-app-bar-nav-icon
            :class="textColor"
            class="d-inline d-md-none"
            @click.stop="drawer = !drawer"
          ></v-app-bar-nav-icon>
        </v-row>
      </v-container>
    </v-app-bar>
    <v-navigation-drawer class="d-md-none" v-model="drawer" absolute temporary right>
      <v-list>
        <v-list-item v-for="link in links" :key="link.id" link>
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
  data() {
    return {
      links: [
        { text: 'Inicio', href: '#index' },
        { text: 'Sobre mi', href: '#about' },
        { text: 'Conocimientos', href: '#index' },
        { text: 'Portafolio', href: '#index' },
        { text: 'Contactame', href: '#index' }
      ],
      scrollPosition: null,
      scrollDefault: 50,
      textColor: 'white--text',
      color: 'transparent',
      logo: '/logo-dark.png',
      flat: true,
      drawer: null
    }
  },
  watch: {
    scrollPosition(newValue) {
      if (this.scrollPosition < this.scrollDefault) {
        this.textColor = 'white--text'
        this.color = 'transparent'
        this.logo = '/logo-dark.png'
        this.flat = true
      } else {
        this.textColor = 'black--text'
        this.color = 'grey lighten-2'
        this.logo = '/logo-light.png'
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
</style>