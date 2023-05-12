<template>
    <div>
      <div>




        
      </div>





    </div>
</template>

<script >
export default {
  name: 'Vote',
  data: () => ({
    drawer: null,
    tab: 0,
    model: '',
    search: null,
    movies: [],
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
    titleRowHeight: 10,

  }),
  watch: {
    group() {
      this.drawerRight = false
    },
  },
  mounted() {
    this.loadMovies();
    document.title = '2023'
  },
  methods: {
    loadMovies: async function () {
      try {
        const response = await this.$http.get("/movie/popular");
        this.movies = response.data.results;

      } catch (error) {
        console.log(error);
      }
    },
    changes(tab) {
      document.title = tab
    }
  }
}
</script>
