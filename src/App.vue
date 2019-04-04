<template>
<div>
 <Nav />
  <div class="container" id="main>
 <div class="alert alert-danger" role="alert" v-for="(e, i) in Globals.errors" :key="i" >
	        <button type="button" class="close" aria-label="Close" @click="Globals.deleteError(i)">
	          <span aria-hidden="true">&times;</span>
	        </button>
	        <strong>{{e.msg}}</strong> 
	      </div>
  <router-view/>
  </div>
  </div>
</template>

<script>
import Nav from "@/components/Nav";
import  { Globals } from "@/models/api";
export default {
	  data: ()=>({
	    Globals: Globals
	  }),
	components: {
	    Nav
	  }
</script>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
