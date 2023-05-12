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
      rate: 4.4,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Ballinciaga.png?w=781&ssl=1',
      des: 'Ballinciaga har gått fra å produsere russelåter i hopetall til å skape musikk som får folk i hele landet til å danse på bordet.'
    },
    {
      name: "Undergrunn",
      rate: 4.3,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Undergrunn.png?w=781&ssl=1.jpg',
      des: 'Undergrunn har tilsynelatende fått kulturell kapital fora med morsmelka. Rapgruppa er unge og vitale, og balanserer klassisk rapstil med lekne melodier.'
    },
    {
      name: "Synne Vo",
      rate: 4.6,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/SynneVo.png?w=781&ssl=1.jpg',
      des: 'Synne Vo er en hitmaskin som ikke kun skriver fengende låter om eget liv, men som også skriver popperler for andre artister.'
    },{
      name: "Ramón",
      rate: 4.5,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Ramon.png?fit=781%2C904&amp;ssl=1.jpg',
      des: 'Ramón ble kjent for hele Norge over natta da han med «Ok jeg lover» satte ny norsk strømme-rekord med drøyt 600.000 avspillinger på ett døgn.'
    },
    {
      name: "Karpe",
      rate: 4.8,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Karpe.png?fit=781%2C904&amp;ssl=1',
      des: 'Karpe har ikke bare slått norske konsertrekorder med ti ganger Oslo Spektrum i år. De er også med på å redefinere vår oppfattelse av hva en konsertopplevelse kan være.'
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