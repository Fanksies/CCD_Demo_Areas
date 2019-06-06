<template>
  <v-app>
    <v-content>
      <div id="app">
        <v-container grid-list-lg>
          <v-layout row wrap>
            <v-flex
              xs-12
            >
            <div class="yeh text-xs-center mb-4 elevation-3 display-3 p-4 font-weight-bold py-2 px-4">
              Áreas</div></v-flex>
          </v-layout>
          <v-layout row wrap>
            <v-flex xs12 sm6>
              <Area/>
              <Area2 class="mt-4"/>
              <Area3 class="mt-4"/>
              <Area4 class="mt-4"/>
            </v-flex>
            <v-flex xs12 sm6>
              <Area5 />
              <Area6 class="mt-4" />
              <Area7 class="mt-4" />
            </v-flex>
          </v-layout>
        </v-container>
      </div>
    </v-content>
  </v-app>
</template>

<style lang="scss">
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
  text-transform:uppercase;
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
  max-width:420px;
}

.headline {
  margin-bottom:.35em;
}
</style>



<script>
import Area from "@/components/Area.vue";
import Area2 from "@/components/Area2.vue";
import Area3 from "@/components/Area3.vue";
import Area4 from "@/components/Area4.vue";
import Area5 from "@/components/Area5.vue";
import Area6 from "@/components/Area6.vue";
import Area7 from "@/components/Area7.vue";

export default {
  name: "Areas",
  components: {
    Area,
    Area2,
    Area3,
    Area4,
    Area5,
    Area6,
    Area7
  },
  data: function() {
    return {
      areas: [{ id: 1, title: "yea boi" }]
    };
  }
};
</script>