<template>
  <v-data-table
    headers="black"
    :headers="headers"
    :items="items"
    :items-per-page="itemsPerPage"
    :page.sync="page"
    class="elevation-1 custom-table"
  >
    <template v-slot:item.game_and_event_name="{ item }">
      <v-row class="d-flex">
        <v-img
          class="mr-3"
          max-height="40"
          max-width="40"
          src="/company-log.svg">

        </v-img>
        <span class="mt-3">
                  {{ item.game_and_event_name }}
        </span>
      </v-row>

    </template>
    <template v-slot:item.starts="{ item }">
      {{ item.starts }}
    </template>
    <template v-slot:item.duration="{ item }">
      {{ item.duration }}
    </template>
    <template v-slot:item.registered="{ item }">
      {{ item.registered }}
    </template>
    <template v-slot:item.pool_prize="{ item }">
      {{ item.pool_prize }}
    </template>
    <template v-slot:no-results>
      No matching records found
    </template>
    <template v-slot:footer>
      <v-pagination
        v-model="page"
        :length="totalPages"
        class="mx-4"
      ></v-pagination>
    </template>
  </v-data-table>
</template>

<script>
export default {
  data() {
    return {
      headers: [
        {
          text: 'Game & Event Name',
          value: 'game_and_event_name',
          width: '40%'
        },
        {
          text: 'Starts',
          value: 'starts',

        },
        {
          text: 'Duration',
          value: 'duration',
        },
        {
          text: 'Registered',
          value: 'registered',
        },
        {
          text: 'Pool prize',
          value: 'pool_prize',
        },
      ],
      items: [
        {
          game_and_event_name: 'Game 1, Event 1',
          starts: '2023-04-01 14:00:00',
          duration: '2 hours',
          registered: 50,
          pool_prize: '$1000',
        },
        {
          game_and_event_name: 'Game 2, Event 1',
          starts: '2023-04-02 16:00:00',
          duration: '3 hours',
          registered: 75,
          pool_prize: '$1500',
        },
        {
          game_and_event_name: 'Game 2, Event 1',
          starts: '2023-04-02 16:00:00',
          duration: '3 hours',
          registered: 75,
          pool_prize: '$1500',
        }, {
          game_and_event_name: 'Game 2, Event 1',
          starts: '2023-04-02 16:00:00',
          duration: '3 hours',
          registered: 75,
          pool_prize: '$1500',
        }, {
          game_and_event_name: 'Game 2, Event 1',
          starts: '2023-04-02 16:00:00',
          duration: '3 hours',
          registered: 75,
          pool_prize: '$1500',
        }, {
          game_and_event_name: 'Game 2, Event 1',
          starts: '2023-04-02 16:00:00',
          duration: '3 hours',
          registered: 75,
          pool_prize: '$1500',
        }, {
          game_and_event_name: 'Game 2, Event 1',
          starts: '2023-04-02 16:00:00',
          duration: '3 hours',
          registered: 75,
          pool_prize: '$1500',
        }, {
          game_and_event_name: 'Game 2, Event 1',
          starts: '2023-04-02 16:00:00',
          duration: '3 hours',
          registered: 75,
          pool_prize: '$1500',
        }, {
          game_and_event_name: 'Game 2, Event 1',
          starts: '2023-04-02 16:00:00',
          duration: '3 hours',
          registered: 75,
          pool_prize: '$1500',
        },






        // more items...
      ],
      itemsPerPage: 10,
      page: 1,
    }
  },
  computed: {
    totalPages() {
      return Math.ceil(this.items.length / this.itemsPerPage)
    },
  },
}
</script>

<style scoped lang="scss">
.custom-table th {
  background-color: black;
  color: black;
}

</style>
