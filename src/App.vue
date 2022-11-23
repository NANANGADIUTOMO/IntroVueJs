<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <h1>{{nama}}</h1>
    <h2>ini anggota saya {{ anggota[0]}}</h2>

    <button 
    v-on:click="gantinama">Ganti nama 
    </button>

    <h2>{{totalBelanja}}</h2>
    <button 
    v-on:click="gantiquantity">Ganti Qty 
    </button>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data : function(){
    return{
      nama : "Paguyuban Magicom Sakti",
      anggota : ["bagas", "alif", "ayom"],
      quantity: 5
    }
  },
  methods:{
    gantinama : function(){
      if(this.nama == "Paguyuban Magicom Sakti"){
          this.nama = "paguyuban centong Kebak"
      }else{
        this.nama = "Paguyuban Magicom Sakti"
      }
    },
    gantiquantity : function(){
      this.quantity++
    }
  },
  computed:{
    totalBelanja :   function(){
      return this.quantity * 10000
    }
  },
  components: {
    //HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
