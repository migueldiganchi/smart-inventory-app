<template>
  <v-layout column justify-center align-center>
    <v-flex>

      <div class="pa-3 text-xs-center">

        <h2 class="text-xs-center primary--text pa-3 mb-3">
          Productos faltantes
        </h2>

        <div>
          <h3>Coca cola</h3>
          <v-progress-linear
            color="warning"
            height="15"
            value="12"
          ></v-progress-linear>
        </div>

        <div>
          <h3>Vasos de whisky</h3>
          <v-progress-linear
            color="warning"
            height="15"
            value="4"
          ></v-progress-linear>
        </div>

        <div>
          <h3>Vasos de whisky</h3>
          <v-progress-linear
            color="warning"
            height="15"
            value="6"
          ></v-progress-linear>
        </div>

        <div>
          <v-btn color="primary" flat nuxt to="/stock">
            Enviar
          </v-btn>
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
