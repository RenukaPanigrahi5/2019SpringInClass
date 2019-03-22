<template>
<div>
 <Nav />
  <div class="container" id="main>
  </div> 
    <router-view/>
  </div>
</template>

<script>
import Nav from "@/components/Nav";
export default {
  components:{
    Nav
  }
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
