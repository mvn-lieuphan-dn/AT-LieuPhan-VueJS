<template>
  <header class="header-pgage">
    <p>{{ titleHeader }}</p>
    <p>{{ title }}</p>
    <button @click="changeTitleHeader">Click in header</button>
  </header>
</template>

<script>
export default {
  name: 'comp-header',
  props: {
    titleHeader: String // định dạng kiểu dữ liệu,
  },
  data() {
    return {
      title: 'Header page'
    }
  },
  methods: {
    changeTitleHeader () {
      // this.title = 'Header from header component!!!';
      // ko ddc phep thay doi prop tu component cha
      // truyen su kien dc thong bao snag ben ngoai
      // kich hoat su kien
      console.log('trước khi kích hoạt sự kiện change title event')
      this.$emit('changeTitleEvent');

    },
    text(e) {
      console.log(e.target)
    }
  }
}
</script>

<style>

</style>