<template>
  <div class="blue__background">
    <v-row>
      <v-col>
        <VoteCard foo= "card"/>
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
  data: () => ({
    card : "homan"
  }),
  // mounted() {
  //   this.card
  // },
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
  max-width: 1274px;
}
</style>