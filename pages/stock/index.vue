<template>
  <v-container class="pa-4" grid-list-lg fluid>
    <ProductList :products="products" />
  </v-container>
</template>

<script>
  import ProductList from '@/components/stock/ProductList'

  export default {
    components: {
      ProductList
    },
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
