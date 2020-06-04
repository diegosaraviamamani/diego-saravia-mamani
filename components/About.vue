<template>
  <v-img min-height="100vh">
    <v-container id="about" wrap>
      <v-row class="py-12" justify="center">
        <v-col cols="12" class="text-center my-12">
          <span class="display-2 text">SOBRE MI</span>
        </v-col>
        <v-col cols="12" md="8">
          <v-tabs
            v-model="tab"
            color="primary"
            slider-color="transparent"
            background-color="transparent"
            grow
            icons-and-text
            show-arrows
          >
            <v-tab v-for="item in items" :key="item.id" class="hvr-sweep-to-bottom">
              {{item.title}}
              <v-icon>{{item.icon}}</v-icon>
            </v-tab>
            <v-tab-item v-for="item in items" :key="item.id">
              <v-card flat>
                <v-card-text class="mx-auto text-center">{{item.content}}</v-card-text>
              </v-card>
            </v-tab-item>
          </v-tabs>
        </v-col>
      </v-row>
    </v-container>
  </v-img>
</template>

<script>
export default {
  data() {
    return {
      tab: null,
      items: [
        {
          title: '¿Quien soy?',
          content:
            'Mi nombre es Diego Saravia Mamani, tengo 26 años, soy boliviano y actualmente vivo en la ciudad de La Paz. Mis hobbies son interpretar musica folclorica (zampoña, quena, guitarra) y armar el cubo Rubik. Soy una persona autodidacta a la que le gusta aprender y poder enseñar lo aprendido. Hace algunos años descubri el mundo del desarrollo web y desde entonces no he dejado de buscar formas de aprendar acerca de el',
          icon: 'face'
        },
        {
          title: 'Estudios',
          content:
            'Egrese a nivel Tecnico Superior de la carrera de Petroleo y Gas Natural, en dicha carrera logre conocer a grandes rasgos el mundo de la programacion y pude despertar un gusto por el analisis y resolucion de problemas empleando algoritmos y diagramas de flujo. Hace un año logre concluir la carrera de Analisis de Sistemas Informaticos y asi poder ampliar mis conocimientos en el area del desarrollo de software',
          icon: 'school'
        },
        {
          title: 'Enseñanza',
          content:
            'Gracias al desempeño que tuve en la universidad, me fue posible ejercer como auxiliar de docencia en materias practicas (Fisica I, Fisica II, Termodinamica); dicha funcion me permitio desarrollar habilidades en la enseñanza que me permitieron ejercer como Instructor de MAT-FIS-QMC en el Programa de Matematica Gauss Newton donde estuve trabajando hasta hace poco y en el cual, gracias a mis estudios, se me encomendo dictar clases de mentorias en programacion basica. ',
          icon: 'book'
        },
        {
          title: 'Experiencia',
          content:
            'Si bien es cierto que actualmente toda mi experiencia laboral se basa en la enseñanza de materias exactas (matematica, fisica, quimica), mi sueño de convertirme en desarrollador web profesional me ha llevado a aprender, por cuenta propia, las distintas tecnologias y frameworks que esta implica, con las cuales he logrado desarrollar paginas web y algunos pequeños proyectos personales',
          icon: 'work'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.text {
  position: relative;
}
.text::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 0;
  right: 0;
  margin: auto;
  width: 70%;
  height: 2px;
  background: #212121;
  border-radius: 1px;
}
.text-center {
  line-height: 2.5em;
  letter-spacing: 0px;
}
</style>