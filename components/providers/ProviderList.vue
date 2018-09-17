<template>
  <v-layout row wrap>
    <v-flex v-for="provider in providers"
      :key="provider.id" xs6>
      <v-card>
        <h3 class="pa-3">
          {{ provider.name }}
        </h3>
        <p class="pb-3 pl-3 pr-3">
          <ul>
            <li><b>Teléfono: </b>{{ provider.contactInfo.phone }}</li>
            <li><b>Celular: </b>{{ provider.contactInfo.mobile }}</li>
            <li><b>Dirección: </b>{{ provider.contactInfo.address }}</li>
          </ul>
        </p>
        <v-divider light></v-divider>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn fab small dark color="purple lighten-2 elevation-1">
              <v-icon dark>location_on</v-icon>
            </v-btn>
            <v-btn fab small  dark color="blue-grey lighten-1 elevation-1">
              <v-icon dark>edit</v-icon>
            </v-btn>
            <v-btn fab small dark color="red elevation-1">
              <v-icon dark>remove</v-icon>
            </v-btn>
          </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
  export default {
    props: {
      providers: {
        type: Array,
        required: true
      }
    }
  };
</script>