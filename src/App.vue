<template>

  <div class="menu">
    <a v-for="menubar in menuitems" :key="menubar">{{menubar}}</a>
  </div>


  <div class="black-bg" v-if="modal==true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용</p>
      <button @click="modal=false">닫기</button>
    </div>
  </div>


  <div>
    <img src="./assets/room1.jpg">
    <h4 @click="modal=true">{{oneroom[0].title}}</h4>
    <p>80만원</p>
  </div>
</template>
<script>

import data from './assets/data.js'

export default {
  name: 'App',
  data(){
    return{
      products: ['역삼동원룸', '천호동원룸', '마포구원룸'],
      menuitems: ['home', 'about', 'products'],
      bbippo: [0,0,0],
      modal: false,
      oneroom:data,
    }
  },
  methods: {
    bbippoclick(){
      this.bbippo++;
    }
  },
  components: {
  }
}
</script>

<style>
body{
  margin: 0;
}
div{
  box-sizing: border-box;
}
.black-bg{
  width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}
.white-bg{
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20pxs;
}
.menu{
  background: darkblue ;
  padding: 15px;
  border-radius: 5px;
}
.menu a{
  color: white;
  padding: 10px;
}
</style>
