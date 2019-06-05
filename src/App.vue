<template>
  <v-app>
    <v-content>
      <div id="app">
        <v-container grid-list-xl>
          <v-layout row xs12 class="mb-4">
                    <div class="yeh text-xs-center mb-4 elevation-3 display-3 p-4 font-weight-bold py-2 px-4">Descubre el CCD</div>
          </v-layout>
          <v-layout row>
            <v-flex xs12 sm6>
              <v-card hover="true" ripple="true">
                <div class="top headline">Laboratorio de VR</div>
                <v-img src="https://i.imgur.com/E3vh2qd.jpg" height="200px"></v-img>

                <v-card-title>
                  <div class="headline">Descubre el poder de realidades mixtas</div>
                  <span
                    class="grey--text"
                  >El laboratorio de inmersión y realidades mixtas es un espacio dedicado a la exploración de estímulos multisensoriales para construir nuevas posibilidades de percepción y acción, así como en la reflexión desde un sentido crítico sobre el estado actual y el futuro de los medios inmersivos. </span>
                </v-card-title>

                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn flat @click="show = !show">
                    Ver Más
                    <v-icon right dark>{{ show ? 'keyboard_arrow_up' : 'keyboard_arrow_down' }}</v-icon>
                  </v-btn>
                </v-card-actions>

                <v-slide-y-transition>
                  <v-container fluid grid-list-md v-show="show" grey lighten-4>
                    <div class="yeh headline text-xs-center mb-4 elevation-3">Miembros</div>

                    <v-layout row wrap color="red">
                      <v-flex
                        v-for="card in cards"
                        :key="card.title"
                        v-bind="{ [`xs${card.flex}`]: true }"
                      >
                        <v-card>
                          <v-img :src="card.src" height="250"></v-img>

                          <v-card-text>
                            <span class="font-weight-medium">Nombre Apellido</span>
                            <span class="grey--text d-block font-weight-medium">Rol</span>
                          </v-card-text>
                        </v-card>
                      </v-flex>
                    </v-layout>
                  </v-container>
                </v-slide-y-transition>
              </v-card>
            </v-flex>

            <v-flex xs12 sm6>
              <v-card hover="true" ripple="true">
                <div class="top headline">Laboratorio de VR</div>
                <v-img src="https://i.imgur.com/E3vh2qd.jpg" height="200px"></v-img>

                <v-card-title>
                  <div class="headline">Descubre el poder de realidades mixtas</div>
                  <span
                    class="grey--text"
                  >El laboratorio de inmersión y realidades mixtas es un espacio dedicado a la exploración de estímulos multisensoriales para construir nuevas posibilidades de percepción y acción, así como en la reflexión desde un sentido crítico sobre el estado actual y el futuro de los medios inmersivos. </span>
                </v-card-title>

                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn flat @click="show = !show">
                    Ver Más
                    <v-icon right dark>{{ show ? 'keyboard_arrow_up' : 'keyboard_arrow_down' }}</v-icon>
                  </v-btn>
                </v-card-actions>

                <v-slide-y-transition>
                  <v-container fluid grid-list-md v-show="show" grey lighten-4>
                    <div class="yeh headline text-xs-center mb-4 elevation-3">Miembros</div>

                    <v-layout row wrap color="red">
                      <v-flex
                        v-for="card in cards"
                        :key="card.title"
                        v-bind="{ [`xs${card.flex}`]: true }"
                      >
                        <v-card>
                          <v-img :src="card.src" height="250"></v-img>

                          <v-card-text>
                            <span class="font-weight-medium">Nombre Apellido</span>
                            <span class="grey--text d-block font-weight-medium">Rol</span>
                          </v-card-text>
                        </v-card>
                      </v-flex>
                    </v-layout>
                  </v-container>
                </v-slide-y-transition>
              </v-card>
            </v-flex>

          </v-layout>
        </v-container>
      </div>
    </v-content>
  </v-app>
</template>

<style lang="scss" scoped>
.top {
  padding: 5px 10px;
  position: absolute;
  z-index: 99;
  background: black;
  top: -14px;
  color: white;
  letter-spacing: 1px;
  border-right: 2px solid white;
  border-bottom: 2px solid white;
  border-radius: 1px;
  // left: -45px;
}
.yeh {
  z-index: 7;
  position: relative;
  padding: 10px;
  background-color: white;
  border-bottom: 3px solid #f04d49;
  // width: ;
  border-right: 3px solid #f04d49;
  margin: 0 auto;
  margin-bottom: 0px;
  letter-spacing: 1px !important;
}
</style>


<script>
export default {
  data: () => ({
    cards: [
      {
        title: "Nombre Apellido",
        src:
          "https://www.centroculturadigital.mx/imgs/areas/marizleth-martinez.jpg",
        flex: 6
      },
      {
        title: "Nombre Apellido",
        src:
          "https://www.centroculturadigital.mx/imgs/areas/hector-guerrero.jpg",
        flex: 6
      },
      {
        title: "Nombre Apellido",
        src:
          "https://www.centroculturadigital.mx/imgs/areas/jacinto-quesnel.jpg",
        flex: 6
      },
      {
        title: "Nombre Apellido",
        src: "https://www.centroculturadigital.mx/imgs/areas/diana-limon.jpg",
        flex: 6
      }
    ],
    show: false
  })
};
</script>