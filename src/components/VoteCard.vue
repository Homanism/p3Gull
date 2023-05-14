<template>
  <div data-aos="fade-up-right" data-aos-duration="3000">
    <v-card :loading="loading" class="vote__card vote_card-cs" max-width="374">
      <template v-slot:loader="{ isActive }">
        <v-progress-linear :active="isActive" color="deep-purple" height="4" indeterminate></v-progress-linear>
      </template>

      <v-img cover height="250" :src="card.link"></v-img>

      <v-card-item>
        <v-card-title>
          {{ card.name }}
        </v-card-title>
      </v-card-item>

      <v-card-text>
        <v-row align="center" class="mx-0">
          <v-rating :model-value="card.rate" color="amber" density="compact" half-increments readonly
            size="small"></v-rating>
          <div class="text-grey ms-4">
            {{ card.rate }}
          </div><br><br><br>
        </v-row>
        <v-divider></v-divider>
        <div>{{ card.des }}</div>
      </v-card-text>
      <v-divider class="mx-4 mb-1"></v-divider>
      <v-btn color="deep-purple-lighten-2" variant="text"
        @click="vote({ cardImg: card.link, cardName: card.name, cardDes: card.des })">
        Stem
      </v-btn>
    </v-card>

  </div>
  <v-dialog v-model="dialog" width="400" :data="dialogData">
    <v-card>
      <v-img contain :src="dialogData.cardImg"></v-img>
      <v-card-text>
        <h2 class="dialogTitle">{{ dialogData.cardName }}</h2>
        <p>

          {{ dialogData.cardDes }}
        </p>
      </v-card-text>
      <v-card-actions>
        <v-btn color="primary" block @click="dialog = false">Close</v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script >
export default {
  props: ['card'],
  name: 'VoteCard',
  // data: () => ({
  //   loading: false,
  //   selection: 1,
  // }),
  data() {
    return {
      dialog: false,
      dialogData: {},
      item: {
        title: "Dialog Title",
        message: "Dialog Message"
      }

    }
  },

  methods: {
    vote(item) {
      debugger
      this.dialogData = item;
      console.log(this.dialogData, 'this.dialogData')
      console.log(item, 'item')
      this.dialog = true
      this.loading = true
      setTimeout(() => (this.loading = false), 2000)
    },
    created() {
      // props are exposed on `this`
      console.log(this.foo)
    },
  }
}
</script>
<style>
@media screen and (max-width: 600px) {
  .vote_card-cs{
    max-width: 100% !important;
    width: 100% !important;
  }
}


</style>
