<template>

  
  <div class="menu">
    <a v-for="(a,i) in menu" :key="i">{{ a }}</a>
  </div>
  <Discount/>
  <div class="item" v-for="(a,i) in product" :key="i">
    <h4 @click="modal = true; selection = i">{{a.title}}</h4>
    <div>
      <img :src="a.image" @click="modal = true; selection = i">
    </div>
  </div>
 
</template>

<script>

import data from './assets/data';
import Discount from './components/Discount.vue';

export default {
  name: 'App',
  data(){
    return{
      selection: 0,
      product : data,
      menu : ['Home', 'Products', 'About'],
      modal: false,
    }
  },

  methods : {
  },

  components: {
    Discount
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
}

.menu{
  background-color: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}


.menu a{
  color: white;
  padding: 10px;
}

body{
  margin: 0;
}

div {
  box-sizing: border-box;
}

.black-bg{
  width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}
img{
  width: 100%;
}

.exitmodal{
  background: transparent;
  border: transparent;
  font-weight: bold;
  font-size: 20px;
}

.item {
  margin-top: 40px;
  margin-bottom: 80px;
}


</style>
