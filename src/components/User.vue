<template>
  <div>
    <p>{{ user.name }} : {{ user.age }}</p>
  </div>
</template>

<script>
export default {
  name: 'user',
  props: {
    user: {
      type: Object,
      default: {}
    }
  },
  data() {
    return {
      title: 'user'
    }
  }
}
</script>

<style>

</style>