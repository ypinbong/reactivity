<template>
  <div class="mainCont">
    <div class="parent">
      <h1>Parent Component</h1>
      <b-form class="my-2" submit="changeText">
        <input v-model="item" type="text">
      </b-form>
      <b-button @click="changeText">
        Send
      </b-button>
    </div>
    <Texttext class="mt-2" :btn-text="item" />
  </div>
</template>
<script>
export default {
  layout: 'blog',
  data () {
    return {
      item: null,
      textToSend: null
    }
  },
  methods: {
    changeText () {
      // this.item = !this.item ? (this.item = 'ajdfj me') : (this.item = null)

      return (this.item = this.textToSend)
    }
  }
}
</script>
<style>
.mainCont {
  display: grid;
  place-items: center;
  height: auto;
}
.child {
  padding: 1rem;
  border: 2px solid black;
}
.parent {
  padding: 1rem;
  margin: 1rem;
  display: grid;
  place-items: center;
}
</style>
