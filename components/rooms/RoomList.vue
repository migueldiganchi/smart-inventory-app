<template>
  <v-layout row wrap> 
    <v-flex xs12 md4 lg2 v-for="room in rooms" :key="room.id">

      <v-card color="blue-grey darken-3 ma-1" 
        class="white--text ">
        <h5 class="text-xs-center pa-3">
          Habitación nº {{ room.number }}
        </h5>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn 
            fab 
            small 
            dark 
            color="grey darken-1 elevation-1">
            <v-icon dark>history</v-icon>
          </v-btn>
          <v-spacer></v-spacer>
          <v-btn 
            fab 
            small 
            dark 
            color="light-blue darken-2 elevation-1">
            <v-icon dark>view_list</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>

    </v-flex>
  </v-layout>
</template>

<script>
  export default {
    props: {
      rooms: {
        type: Array,
        required: true
      }
    }
  };
</script>