<template>
  <div class="child">
    <h2>Child Component</h2>
    <p>{{ getText() }}</p>
  </div>
</template>

<script>
export default {
  props: ['btnText'],
  data () {
    return {
      a: null
    }
  },
  methods: {
    getText () {
      return (this.a = this.btnText)
    }
  }
}
</script>
