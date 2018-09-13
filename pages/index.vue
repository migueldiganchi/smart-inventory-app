<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>

      <div class="text-xs-center mt-3 pa-3">

        <v-avatar
          :size="'124px'"
          color="grey lighten-4"
        >
          <img src="~/assets/media/bot.png" alt="Stock manager">
        </v-avatar>

      </div>

      <div class="pa-3 text-xs-center">

        <h2 class="text-xs-center pa-3 mb-3">
          ¿Qué deseas saber de tu stock?
        </h2>

        <v-textarea
          v-model="bio"
          auto-grow
          box
          color="deep-purple"
          :label="bioPlaceholder"
          rows="3"
        ></v-textarea>

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
