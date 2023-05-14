<template>
  <div class="blue__background">
    <v-row class="vote-card-cs">
     
      <v-col  v-for="card in  cards" :key="card">
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
      rate: 5,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Ballinciaga.png?w=781&ssl=1',
      des: 'Ballinciaga har gått fra å produsere russelåter i hopetall til å skape musikk som får folk i hele landet til å danse på bordet.',
      spotify: 'https://open.spotify.com/embed/track/2kPukYbkTVuvaNn4HhIPBW?utm_source=generator'
    },
    {
      name: "Undergrunn",
      rate: 5,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Undergrunn.png?w=781&ssl=1.jpg',
      des: 'Undergrunn har tilsynelatende fått kulturell kapital fora med morsmelka. De er unge og vitale, og balanserer klassisk rapstil med lekne melodier.',
      spotify: 'https://open.spotify.com/embed/track/3h2IRgTZrU4hSNCePszT23?utm_source=generator'
    },
    {
      name: "Synne Vo",
      rate: 5,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/SynneVo.png?w=781&ssl=1.jpg',
      des: 'Synne Vo er en hitmaskin som ikke kun skriver fengende låter om eget liv, men som også skriver popperler for andre artister.',
      spotify: 'https://open.spotify.com/embed/track/4SY85cjQgYFBx7sIJE562n?utm_source=generator'
    },{
      name: "Ramón",
      rate: 5,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Ramon.png?fit=781%2C904&amp;ssl=1.jpg',
      des: 'Ramón ble kjent for hele Norge over natta da han med «Ok jeg lover» satte ny norsk strømme-rekord med drøyt 600.000 avspillinger på ett døgn.',
      spotify: 'https://open.spotify.com/embed/track/7kSxVn8HvKeHwW3o7W0M2S?utm_source=generator'
    },
    {
      name: "Karpe",
      rate: 5,
      link: 'https://i0.wp.com/p3.no/wp-content/uploads/2022/11/Karpe.png?fit=781%2C904&amp;ssl=1',
      des: 'De har ikke bare slått konsertrekorder med ti ganger. De er også med på å redefinere vår oppfattelse av hva en konsertopplevelse kan være.',
      spotify: 'https://open.spotify.com/embed/track/2wklUkI6nr4uurf5w0AyPz?utm_source=generator'
    }]
  }),
}
</script>
<style>
.blue__background {
  background-color: #32a4eb;
  color: black;
  padding: 2% 2% 2% 2%;
  text-align: center;
  height: auto;
}

@media screen and (max-width: 1430px) {
  .v-col {
  padding-left: 0.5%;
  padding-right: 0.5%;
  /* width: 25%; */
  height: 100%;
  flex-basis: unset !important;
  width: 100%;
}

}
@media screen and (min-width: 1430px) {
  .v-col {
  padding-left: 0.5%;
  padding-right: 0.5%;
  /* width: 25%; */
  width: 280px;
  height: 100%;
}

}
@media (min-width:600px) and (max-width:1024px){
  .v-img__img--cover{
    object-fit: contain !important;
  }
}


.vote-card-cs {
  height:  100%;
  justify-content: center;
}

@media screen and (max-width: 792) {
  .vote-card-cs{
    width: 100%;
    flex-direction: column !important;
    margin: 0;
  }
  .vote-card-cs .v-col {
    width: 100%;
  }
}

</style>
