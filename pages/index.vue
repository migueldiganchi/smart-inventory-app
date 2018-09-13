<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>

      <div class="text-xs-center pa-3">

        <v-avatar
          :size="'124px'"
          color="grey lighten-4"
        >
          <img src="~/assets/media/bot.png" alt="Stock manager">
        </v-avatar>

      </div>

      <div class="pa-3 text-xs-center">

        <h2 class="text-xs-center pa-3">
          ¿Qué deseas saber de tu stock?
        </h2>

         <v-text-field
            v-model="bio"
            box
            color="deep-purple"
            label="Email address"
            type="email"
          ></v-text-field>

          <div class="mt-4" style="border: solid 1px blue;">
            <v-textarea
              v-model="bio"
              auto-grow
              box
              color="deep-purple"
              label="Bio"
              rows="2"
            ></v-textarea>
          </div>
        <div>
          <v-btn color="primary" flat nuxt to="/stock">Continue</v-btn>
        </div>
      </div>
    </v-flex>
  </v-layout>
</template>

<script>
  export default {
    data () {
      return {
        bio: "Some text here",
        bioPlaceholder: '¿Pregunta a tu asistente?',
      }
    }
  };
</script>
