<template>
  <v-container class="pa-4" grid-list-lg fluid>
    <v-layout row wrap>
      <v-flex v-for="product in products"
        :key="product.id" xs12 md6 lg4>
        <v-card 
          color="blue-grey darken-3 ma-1" 
          class="white--text">
            <v-layout row>
              <v-flex xs10>
                <v-card-title primary-title>
                  <div>
                    <label>{{ product.name }}</label>
                    <div 
                      v-for="feature in product.features"
                      :key="feature.id">
                      <small>
                        <b>{{ feature.title }}</b>: <b color="light-green accent-2">{{ feature.value }}</b></small>
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
                  color="light-green accent-3"
                ></v-progress-circular>
              </v-flex>
            </v-layout>
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
  </v-container>
</template>

<script>
  export default {
    data () {
      return {
        products: [
          {
            id: 1,
            name: 'Lata coca-cola',
            value: 91,
            features: [
              { id: 1, title: 'Restante', value: 12 },
              { id: 2, title: 'Mínimo', value: 23 },
            ]
          },
          {
            id: 2,
            name: 'Vaso de whisky',
            value: 53,
            features: [
              { id: 1, title: 'Restante', value: 9 },
              { id: 2, title: 'Mínimo', value: 82 },
            ]
          },
          {
            id: 3,
            name: 'Agua mineral 250cc',
            value: 45,
            features: [
              { id: 1, title: 'Restante', value: 84 },
              { id: 2, title: 'Mínimo', value: 32 },
            ]
          },
          {
            id: 4,
            name: 'Lata coca-cola',
            value: 91,
            features: [
              { id: 1, title: 'Restante', value: 12 },
              { id: 2, title: 'Mínimo', value: 23 },
            ]
          },
          {
            id: 5,
            name: 'Vaso de whisky',
            value: 53,
            features: [
              { id: 1, title: 'Restante', value: 9 },
              { id: 2, title: 'Mínimo', value: 82 },
            ]
          },
          {
            id: 6,
            name: 'Agua mineral 250cc',
            value: 45,
            features: [
              { id: 1, title: 'Restante', value: 84 },
              { id: 2, title: 'Mínimo', value: 32 },
            ]
          },
          {
            id: 7,
            name: 'Lata coca-cola',
            value: 91,
            features: [
              { id: 1, title: 'Restante', value: 12 },
              { id: 2, title: 'Mínimo', value: 23 },
            ]
          },
          // {
          //   id: 8,
          //   name: 'Vaso de whisky',
          //   value: 53,
          //   features: [
          //     { id: 1, title: 'Restante', value: 9 },
          //     { id: 2, title: 'Mínimo', value: 82 },
          //   ]
          // },
          // {
          //   id: 9,
          //   name: 'Agua mineral 250cc',
          //   value: 45,
          //   features: [
          //     { id: 1, title: 'Restante', value: 84 },
          //     { id: 2, title: 'Mínimo', value: 32 },
          //   ]
          // }
        ]
      }
    }
  };
</script>
