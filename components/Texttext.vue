<template>
  <div class="child">
    <h2>Child Component</h2>
    <p>{{ getText() }}</p>
    <h5>Counter: {{ $store.state.text.counter }}</h5>
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
