<template>
  <v-layout column justify-center align-center>
    <v-flex>
      <div class="pa-3 text-xs-center">

        <h2 class="text-xs-center pa-3 mb-3">
          Productos faltantes
        </h2>

        <div>
          <h3>Coca cola</h3>
          <v-progress-linear
            color="light-green accent-3"
            height="15"
            value="12"
          ></v-progress-linear>
        </div>

        <div>
          <h3>Vasos de whisky</h3>
          <v-progress-linear
            color="light-green accent-3"
            height="15"
            value="4"
          ></v-progress-linear>
        </div>

        <div>
          <h3>Vasos de whisky</h3>
          <v-progress-linear
            color="light-green accent-3"
            height="15"
            value="6"
          ></v-progress-linear>
        </div>

      </div>
    </v-flex>
  </v-layout>
</template>

<script>
  export default {
    data () {
      return {
        bio: "",
        bioPlaceholder: 'Pregunta a tu asistente lo que desees saber',
      }
    }
  };
</script>
