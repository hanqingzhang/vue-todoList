<template>
  <div id="app">
    <input v-model="inputValue">
    <button @click="handleClick">增加</button>
    <ul>
      <li
       v-for="(item,index) of list"
      :key="index"
      @click="handleDelete(index)">{{item}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      inputValue:'',
      list:[]

    }
  },
  methods:{
    handleClick(){
      this.list.push(this.inputValue);
      this.inputValue=''
    },
    handleDelete(index){
      this.list.splice(index,1);
      this.inputValue=''
    }

  }

  
}
</script>

<style>

</style>
