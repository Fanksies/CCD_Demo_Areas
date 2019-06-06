<template>
    <v-card hover="true" ripple="true">
      <div class="top headline">Laboratorio Web</div>
      <v-img src="https://i.imgur.com/nxF1dhP.jpg" height="200px"></v-img>

      <v-card-title>
        <div class="headline">Desarrollo web y móvil</div>
        <span
          class="grey--text"
        >Se dedica propiamente al desarrollo de las plataformas web y móvil del CCD. Busca soluciones funcionales, visuales, interactivas y creativas para extender los alcances del programa del CCD más allá de su espacio físico.</span>
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
  name: "Area5",
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
