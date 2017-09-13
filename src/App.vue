<template>
  <div id="app" class="app">
    <v-header :header="header"></v-header>
    <router-view></router-view>
  </div>
</template>

<script>
import Header from '@/components/header/header'
import axios from 'axios'
export default {
  data(){
    return {
      header:{}
    }
  },
  components:{
    'v-header':Header
  },
  created(){
     axios.get('/static/data.json').then(res=>{
          this.header=res.data.header;
     },err=>{
          console.log(err);
     })
  }
}
</script>

<style>

</style>
