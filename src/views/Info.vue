<template>
  <div>
    hello info component
    <button type="button" @click="add()">添加</button>
  </div>
</template>

<script>
  // @符号代表src目录，store.js的.js后缀可以省略
  import store from '@/store';
  export default {
    name: 'Info',
    store,
    data() {
      return {
        msg: 'hello msg'
      }
    },
    mounted (){
      // 调试方法，window.vue这时候是info这个组件
      window.vue = this
    },
    methods: {
      add() {
        console.log('add Event from info!');
        debugger
        store.commit('increase')
      },
      output(){
        console.log("in output")
      }
    },
  };
</script>

<style scoped>

</style>
