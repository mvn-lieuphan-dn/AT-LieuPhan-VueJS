<template>
  <div id="app">
    <button @click="title = 'Thay doi title trong app.vue'">Click in app</button>
    <!-- Thay đổi dữ lieuj tại cha và ngay lập tức con nhận đc sự thay đổi -->
    <comp-header v-bind:titleHeader="title" v-on:changeTitleEvent="changeTitleInApp"></comp-header>
    <list-user v-bind:arrUsers="arrUser"></list-user>
    <comp-footer v-bind:title="title"></comp-footer>
  </div>
</template>
<script>
// v-on:changeTitleEvent="changeTitleInApp"
// changeTitleEvent: ten su kien
// changeTitleInApp: ham xu li
import CompHeader from './components/CompHeader';
import CompFooter from './components/CompFooter';
import ListUser from './components/ListUser';
export default {
  name: 'app',
  data () {
    return {
      arrUser: [
        { name: 'ksjdi', age: 18 },
        { name: 'ksjdi', age: 18 },
        { name: 'ksjdi', age: 18 },
        { name: 'ksjdi', age: 18 }
      ],
      title: 'Header - Hello Vue JS',
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    changeTitleInApp() {
      console.log('handle title header');
    }
  }
  ,
  components: {
    CompHeader,
    CompFooter,
    ListUser
  }
}
</script>
<style>
/* 
Props : truyền dữ liệu từ cha sang con
Cú pháp giống vs thuộc tính
 */
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
