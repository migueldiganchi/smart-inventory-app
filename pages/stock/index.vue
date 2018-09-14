<template>
  <v-container grid-list-lg>
    <v-layout row wrap>
      <v-flex v-for="product in products" xs12 md6 lg4>
        <v-card color="blue-grey darken-3" class="white--text">
            <v-layout row>
              <v-flex xs10>
                <v-card-title primary-title>
                  <div>
                    <label>{{ product.name }}</label>
                    <div v-for="feature in product.features">
                      <small><b>{{ feature.title }}</b>: {{ feature.value }}</small>
                    </div>
                  </div>
                </v-card-title>
              </v-flex>
              <v-flex xs3 class="pt-4 mt-1 mr-3 text-xs-right">
                <v-progress-circular
                  :rotate="360"
                  :size="60"
                  :width="6"
                  :value="product.value"
                  color="teal"
                ></v-progress-circular>
              </v-flex>
            </v-layout>
            <v-divider light></v-divider>
            <v-card-actions class="pa-3">
              Rate this album
              <v-spacer></v-spacer>
              <v-icon>star_border</v-icon>
              <v-icon>star_border</v-icon>
              <v-icon>star_border</v-icon>
              <v-icon>star_border</v-icon>
              <v-icon>star_border</v-icon>
            </v-card-actions>
          </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        products: [
          {
            name: 'Lata coca-cola',
            value: 91,
            features: [
              { title: 'Restante', value: 12 },
              { title: 'Mínimo', value: 23 },
            ]
          },
          {
            name: 'Vaso de whisky',
            value: 53,
            features: [
              { title: 'Restante', value: 9 },
              { title: 'Mínimo', value: 82 },
            ]
          },
          {
            name: 'Agua mineral 250cc',
            value: 45,
            features: [
              { title: 'Restante', value: 84 },
              { title: 'Mínimo', value: 32 },
            ]
          },
          {
            name: 'Lata coca-cola',
            value: 91,
            features: [
              { title: 'Restante', value: 12 },
              { title: 'Mínimo', value: 23 },
            ]
          },
          {
            name: 'Vaso de whisky',
            value: 53,
            features: [
              { title: 'Restante', value: 9 },
              { title: 'Mínimo', value: 82 },
            ]
          },
          {
            name: 'Agua mineral 250cc',
            value: 45,
            features: [
              { title: 'Restante', value: 84 },
              { title: 'Mínimo', value: 32 },
            ]
          },
          {
            name: 'Lata coca-cola',
            value: 91,
            features: [
              { title: 'Restante', value: 12 },
              { title: 'Mínimo', value: 23 },
            ]
          },
          {
            name: 'Vaso de whisky',
            value: 53,
            features: [
              { title: 'Restante', value: 9 },
              { title: 'Mínimo', value: 82 },
            ]
          },
          {
            name: 'Agua mineral 250cc',
            value: 45,
            features: [
              { title: 'Restante', value: 84 },
              { title: 'Mínimo', value: 32 },
            ]
          }
        ]
      }
    }
  };
</script>
