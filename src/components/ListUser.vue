<template>
  <div>
    <p>{{ title }}</p> 
    <user v-for="(item, index) in arrUsers"
     v-bind:key="index"
     v-bind:user="item"
     />
  </div>
</template>

<script>
import User from './User.vue';
export default {
  name: 'list-user',
  props: {
    arrUsers: {
      type: Array,
      default: []
    }
  },
  data() {
    return {
      title: 'List User'
    }
  },
  components: {
    User
  }
}
</script>

<style>

</style>