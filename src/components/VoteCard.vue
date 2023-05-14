<template>
  <div class="aos" data-aos="fade-up-right" data-aos-duration="3000">
    <v-card  class="vote__card vote_card-cs" >
      <template v-slot:loader="{ isActive }">
        <v-progress-linear :active="isActive" color="deep-purple" height="4" indeterminate></v-progress-linear>
      </template>

      <v-img cover height="250" :src="card.link"></v-img>

      <v-card-item>
        <v-card-title>
          {{ card.name }}
        </v-card-title>
      </v-card-item>
      <!-- <v-rating :model-value="card.rate" class="vote-card-star" color="amber" density="compact" half-increments readonly
           size="small"></v-rating> -->
           <div class="spotify-embed">
             <!-- <iframe src="https://embed.spotify.com/?uri=spotify:user:oosabaj:playlist:2UDe8QqHAXUaLrdb0QsDGE" width="250" height="80" frameborder="0" allowtransparency="true"> -->
             <iframe :src="card.spotify" width="250" height="80" frameborder="0" allowtransparency="true">
          </iframe>
          </div>
      <!-- <v-card-text>
        <v-divider></v-divider>
        <div class="card__des">{{ card.des }}</div>
      </v-card-text> -->
      <v-divider class="mx-4 mb-1"></v-divider>
      <v-btn color="blue-lighten-2" variant="text"
        @click="vote({ cardImg: card.link, cardName: card.name, cardDes: card.des })">
        Stem
      </v-btn>
    </v-card>

  </div>
  <v-dialog v-model="dialog" width="400" :data="dialogData">
    <v-card>
      <v-img contain :src="dialogData.cardImg"></v-img>
      <v-card-text>
        <h2 class="dialogTitle">Du stemte på {{ dialogData.cardName }}</h2>
        <v-divider></v-divider>
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

/* .spotify-embed {
  background: #282828;
} */

.aos{
    height: 100%;
  }

  .vote-card-star {
    justify-content: center;
  }

  .vote__card {
    height: 100%;
    display: flex !important;
    flex-direction: column !important;
  }

@media screen and (max-width: 792) {
  .vote_card-cs{
    max-width: 100% !important;
    width: 100% !important;
  }
  .card__des {
    /* height: 800px; */
    background-color: red;
  }
}

@media screen and (max-width: 992.5px) {
.vote_card-cs{
    max-width: 800% !important;
    width: 100% !important;
  }
}
@media screen and (min-width: 792) and (max-width: 950px) {
  .vote_card-cs{
    max-width: 800% !important;
    width: 100% !important;
    background-color: blue;
  }
  .card__des {
    height: 250px;
    background-color: blue;
  }
}

</style>
