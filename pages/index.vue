  <template>
  <v-layout row wrap>
    <v-flex md4>
      <div class="pa-3 text-xs-right">
        <p class="my-3">
          Quedan 34 unidades de Coca-Cola
        </p>
        <v-divider></v-divider>
        <p class="my-3">
          <b>Rubén</b> ha agregado 5 <b>latas de coca</b>
        </p>
        <v-divider></v-divider>
        <p class="my-3">
          <b>Julian</b> ha quitado 3 <b>vasos de wiskey</b>
        </p>
      </div>
    </v-flex>

    <v-flex md8 class="text-xs-center">
      <div class="pa-3 text-xs-right">
        <v-layout row wrap>
          <v-flex
            v-for="(item, i) in items"
            :key="i" 
            xs12 sm6 md3>

            <v-card class="ma-3 nuxt-link"
              nuxt="true"
              :to="item.to"
              color="blue-grey darken-3 ">
              <div class="text-xs-center pt-3">
                <v-icon lg right color="primary">
                  {{ item.icon }}
                </v-icon>
                <h4 class="mb-1 pa-3 text--primary">
                  {{ item.title }}
                </h4>
              </div>
              <!-- <div class="pa-2">
                <v-btn
                  block
                  flat
                  small
                  :disabled="false"
                  color="primary"
                  nuxt="true"
                  :to="item.to"
                  @click.native="loader = 'loading3'"
                >
                  Entrar
                </v-btn>
              </div> -->
            </v-card>
          </v-flex>
        </v-layout>
      </div>
    </v-flex>
  </v-layout>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          { icon: 'equalizer', title: 'Stock', to: '/stock' },
          { 
            icon: 'account_balance_wallet',
            title: 'Proveedores',
            to: '/providers'
          },
          { 
            icon: 'meeting_room', 
            title: 'Habitaciones', 
            to: '/rooms' 
          },
          { icon: 'android', title: 'Asistente', to: '/assistant' }
        ],
        activities: [
          {
            id: 1,
            user: {
              name: 'Eduardo'
            },
            description: 'Agregado'
          }
        ]
      }
    }
  };
</script>
