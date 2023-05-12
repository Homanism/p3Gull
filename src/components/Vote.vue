<template>
  <div class="blue__background">
    <v-row>
      <v-col v-for="card in  cards" :key="card">
        <VoteCard :card="card" />
      </v-col>
    </v-row>
  </div>
</template>

<script >
import VoteCard from './VoteCard.vue'

export default {
  name: 'Vote',
  components: {
    VoteCard,
  },
  data: () => ({
    cards: [{
      name: "Ballinciaga",
      rate: 4.8,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Ballinciaga.png?w=781&ssl=1',
      des: 'Ballinciaga har gått fra å produsere russelåter i hopetall til å skape musikk som får folk i hele landet til å danse på bordet.'
    },
    {
      name: "Ballinciaga",
      rate: 4.8,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Ballinciaga.png?w=781&ssl=1',
      des: 'Ballinciaga har gått fra å produsere russelåter i hopetall til å skape musikk som får folk i hele landet til å danse på bordet.'
    },
    {
      name: "Ballinciaga",
      rate: 4.8,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Ballinciaga.png?w=781&ssl=1',
      des: 'Ballinciaga har gått fra å produsere russelåter i hopetall til å skape musikk som får folk i hele landet til å danse på bordet.'
    },{
      name: "Ballinciaga",
      rate: 4.8,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Ballinciaga.png?w=781&ssl=1',
      des: 'Ballinciaga har gått fra å produsere russelåter i hopetall til å skape musikk som får folk i hele landet til å danse på bordet.'
    },
    {
      name: "Ballinciaga",
      rate: 4.8,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Ballinciaga.png?w=781&ssl=1',
      des: 'Ballinciaga har gått fra å produsere russelåter i hopetall til å skape musikk som får folk i hele landet til å danse på bordet.'
    }]
  }),
}
</script>
<style>
.blue__background {
  background-color: #32a4eb;
  color: black;
  padding: 2% 0% 2% 2%;
  text-align: center;
}

.v-col {
  padding-left: 0;
  padding-right: 1%;
}

.v-row {
  justify-content: center;
}
</style>