
<template>
  <v-app dark>
    <v-navigation-drawer
      :mini-variant="miniVariant"
      :clipped="clipped"
      v-model="drawer"
      fixed
      app
    >
      <v-list>
        <v-list-tile
          router
          :to="item.to"
          :key="i"
          v-for="(item, i) in items"
          exact
        >
          <v-list-tile-action>
            <v-icon>
              {{ item.icon }}
            </v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title v-text="item.title"></v-list-tile-title>
          </v-list-tile-content>

        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar fixed app :clipped-left="clipped">
      <v-toolbar-side-icon @click="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title v-text="title"></v-toolbar-title>
      <v-spacer></v-spacer>
      <v-text-field
        class="mt-2"
        flat
        label="Buscar producto"
        solo-inverted
      ></v-text-field>
      <v-btn icon>
        <v-icon>search</v-icon>
      </v-btn>
    </v-toolbar>
    <v-content>
      <nuxt />
    </v-content>
    <v-footer
      class="elevation-21" 
      app>
      <span>&copy; 2017</span>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    watch: {
      $route () {
        this.drawer = !this.drawer
      }
    },
    data() {
      return {
        clipped: false,
        drawer: false,
        fixed: false,
        items: [
          { icon: 'home', title: 'Inicio', to: '/' },
          { icon: 'equalizer', title: 'Stock', to: '/stock' },
          { 
            icon: 'account_balance_wallet', 
            title: 'Proveedores', 
            to: '/providers' 
          },
          { icon: 'android', title: 'Asistente', to: '/assistant' }
        ],
        miniVariant: false,
        title: 'StockBot'
      }
    }
  };
</script>
