<template>
    <v-card hover="true" ripple="true">
      <div class="top headline">Juegos</div>
      <v-img src="https://i.imgur.com/Z89OYA0.jpg" height="200px"></v-img>

      <v-card-title>
        <div class="headline">Juegos</div>
        <span
          class="grey--text"
        >Espacios activos donde ocurren game jams, hackatones, charlas y eventos ligados al ludismo, el arte y la cultura colectiva. Es un proyecto incluyente, vincula de manera autogestiva a niños, jóvenes, profesionales y comunidades diversas para mejorar sus habilidades digitales, fortalecer la equidad, generar vínculos, promover la conciencia ciudadana y apoyar la innovación y el emprendimiento. Entendemos al jugador como un ente en constante hacer y compartir.</span>
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
            <v-flex v-for="card in cards" :key="card.title" v-bind="{ [`xs${card.flex}`]: true }">
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
</template>

<script>
export default {
  name: "Area2",
  props: {
    parentData: Object
  },
  data: () => ({
    show:false,
  })
};
</script>

<style>
</style>
