<template>
    <v-card hover="true" ripple="true">
      <div class="top headline">Tecnologías Libres</div>
      <v-img src="https://i.imgur.com/TiQfyHa.jpg" height="200px"></v-img>

      <v-card-title>
        <div class="headline">Rompiendo la línea entre consumidor y producto</div>
        <span
          class="grey--text"
        >En esta área se busca romper la delgada línea que separa a un consumidor de un productor de tecnología, esto se logra desmitificando la propia tecnología y haciéndola accesible.
Aquí se diseñan y manufacturan prototipos de software y hardware que se presentan al público en general, despejando toda duda existente de su funcionamiento, todo lo que se genera se comparte, incluyendo código, esquemas y planos, además se realizan asesorías y talleres. El principal objetivo es que sea utilizado y modificado por los visitantes del CCD para solucionar algún problema dentro de su entorno. </span>
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
  name: "Area7",
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
