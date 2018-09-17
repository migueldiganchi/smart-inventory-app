<template>
  <v-container class="pa-4" grid-list-lg fluid>
    <ProviderList :providers="providers" />
  </v-container>
</template>

<script>
  import ProviderList from '@/components/providers/ProviderList'

  export default {
    components: {
      ProviderList
    },
    data () {
      return {
        providers: [
          {
            id: 1,
            name: 'Distribuidora Santiago',
            contactInfo: {
              phone: '999999',
              mobile: '999999',
              address: 'Roca norte 4564, la Banda',
              location: {
                latitude: 999,
                longitude: 999
              },

            }
          },
          {
            id: 2,
            name: 'Envases del norte',
            contactInfo: {
              phone: '999999',
              mobile: '999999',
              address: 'Belgrano sur 3243, Santiago del estero',
              location: {
                latitude: 999,
                longitude: 999
              },

            }
          },
          {
            id: 3,
            name: 'Fiambrería Cachito',
            contactInfo: {
              phone: '999999',
              mobile: '999999',
              address: 'Olaichea 99, Santiago del estero',
              location: {
                latitude: 999,
                longitude: 999
              },

            }
          },
          {
            id: 4,
            name: 'Panadería Los abuelos',
            contactInfo: {
              phone: '999999',
              mobile: '999999',
              address: 'Jujuy 432, Santiago del estero',
              location: {
                latitude: 999,
                longitude: 999
              },

            }
          }
        ]
      }
    }
  };
</script>