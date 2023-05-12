<template>
  <div class="blue__background__color">
    <h1>Hvem bør vinne «Årets artist»?</h1>
    <v-row>
      <v-col class="voteCard__col">
        <VoteCard />
      </v-col>
      <v-col>
        <VoteCard />
      </v-col>
      <v-col>
        <VoteCard />
      </v-col>
      <v-col>
        <VoteCard />
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
}
</script>
<style>
.blue__background__color {
  background-color: #32a4eb;
  color: black;
  padding: 2% 0% 2% 2%;
  text-align: center;
}

.voteCard__col{
  padding-left: 0;
  padding-right: 0;
}
</style>