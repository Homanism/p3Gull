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
