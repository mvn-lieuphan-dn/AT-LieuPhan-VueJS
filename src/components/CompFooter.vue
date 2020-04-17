<template>
  <footer>
  <p>{{ title }}</p>
  <button v-on:click="test">a</button>
  </footer>
</template>

<script>
export default {
  name: 'comp-footer',
  methods: {
    test(e) {
      console.log(e);
    }
  },
  props: {
    title: {
      type: String,
      default: 'footer'
  }
  },
  data() {
    return {
      // title: 'Footer page'
    }
  }
}
</script>

<style>

</style>