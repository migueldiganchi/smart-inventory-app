<template>
  <v-container class="pa-4" grid-list-lg fluid>
    <RoomList :rooms="rooms" />
  </v-container>
</template>

<script>
  import RoomList from '@/components/rooms/RoomList'

  export default {
    components: {
      RoomList
    },
    data () {
      return {
        rooms: [
          {
            id: 1,
            number: 3
          },
          {
            id: 2,
            number: 33
          },
          {
            id: 3,
            number: 15
          },
          {
            id: 4,
            number: 99
          },
          {
            id: 5,
            number: 9
          },
          {
            id: 6,
            number: 12
          },
          {
            id: 7,
            number: 15
          }
        ]
      }
    }
  };
</script>