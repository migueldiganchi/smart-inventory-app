<template>
  <v-layout row wrap>
    <v-flex v-for="product in products"
      :key="product.id" xs12 md4 lg3>

      <v-card 
        color="blue-grey darken-3 ma-1" 
        class="white--text">
          <v-card-title primary-title>
            <div>
              <label>{{ product.name }}</label>
            </div>
          </v-card-title>

          <v-progress-linear
            height="15"
            :value="product.value"
            color="light-green accent-3"
          ></v-progress-linear>

          <div class="pa-1">
            <div class="mr-1 text-xs-center"
              v-for="feature in product.features"
              :key="feature.id">
              <small>
                <b>{{ feature.title }}</b>: <b color="light-green accent-2">{{ feature.value }}</b></small>
            </div>
          </div>

          <v-divider light></v-divider>
          <v-card-actions>
            <v-btn fab small dark color="indigo elevation-1">
              <v-icon dark>timeline</v-icon>
            </v-btn>
            <v-spacer></v-spacer>
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
      products: {
        type: Array,
        required: true
      }
    }
  };
</script>