<template>
  <v-navigation-drawer v-model="drawerRight" location="right">
    <v-img src="https://info.nrk.no/wp-content/uploads/2019/09/NRKP3-hovedlogo_c_RGB.jpg"> </v-img>
    <v-list :items="items"></v-list>
  </v-navigation-drawer>
  <v-app-bar app color="black" dark prominent>
    <v-icon class="mr-2">mdi-hexagon-multiple</v-icon>
    <v-toolbar-title>
      <v-img class='NavBar__Img' src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQvsOEzRWRPeI66HiLZiSHESRhifcIg37mg8w&usqp=CAU.jpg">
      </v-img>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-autocomplete clearable hide-no-data hide-selected color="white" label="search" prepend-inner-icon="search" flat
      :items="movies" item-text="title" item-value="id" id="search">
      <template v-slot:item="{ item }">
        <v-btn :to="`/item/${item.id}`">{{ item.title }}</v-btn>
      </template>
    </v-autocomplete>
    <v-btn icon>
      <v-badge color="blue" content="2" overlap>
        <v-icon>mdi-bell-ring</v-icon>
      </v-badge>
    </v-btn>
    <v-badge bordered bottom color="blue" dot offset-x="5" offset-y="5">
      <v-avatar size="40">
        <v-img src="https://i0.wp.com/norskiransk.no/wp-content/uploads/2023/02/homan01.jpg?fit=300%2C300&ssl=1"></v-img>
      </v-avatar>
    </v-badge>
    <v-app-bar-nav-icon variant="text" @click.stop="drawerRight = !drawerRight"></v-app-bar-nav-icon>
  </v-app-bar>
</template>

<script >
export default {
  name: 'NavBar',
  data: () => ({
    drawer: null,
    tab: 0,
    model: '',
    search: null,
    drawerRight: false,
    group: null,
    items: [
      {
        title: 'Morten',
        value: 'Morten',
      },
      {
        title: 'Camila',
        value: 'Camila',
      },
      {
        title: 'Martine ',
        value: 'Martine ',
      },
      {
        title: 'Homan',
        value: 'Homan',
      },
    ],
    titleRowHeight: 10

  }),
  watch: {
    group() {
      this.drawerRight = false
    },
  },
  mounted() {
    document.title = '2023'
  },
  methods: {
    changes(tab) {
      document.title = tab
    }
        }
}
</script>
<style>
.NavBar__Img {
  max-width: 15%;
  height: 100px;
}
</style>
