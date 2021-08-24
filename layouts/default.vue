<template>
  <div>
    <div class="navbar">
      <h2>Layout</h2>
      <b-button @click="add_one">
        Add+
      </b-button>
    </div>
    <Nuxt />
  </div>
</template>

<script>
export default {
  data () {
    return {
      item: null,
      textToSend: null
    }
  },
  methods: {
    add_one () {
      this.$store.commit('text/increment')
    },
    changeText () {
      // this.item = !this.item ? (this.item = 'ajdfj me') : (this.item = null)
      this.item = this.textToSend
      this.textToSend = null
    }
  }
}
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: center;
  flex-direction: column;
  top: 0;
  border-bottom: 3px solid black;
}
</style>
