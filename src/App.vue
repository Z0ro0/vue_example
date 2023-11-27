<template>

  <div class="menu">
    <a v-for="menubar in menuitems" :key="menubar">{{menubar}}</a>
  </div>

  <div>
    <h4>{{products[0]}}</h4>
    <p>80만원</p>
    <button @click="bbippoclick">허위매물신고</button>
    <span>신고수 :{{ bbippo  }}</span>
  </div>
  <div>
    <h4>{{products[1]}}</h4>
    <p>70만원</p>
  </div>
  <div>
    <h4>{{products[2]}}</h4>
    <p>50만원</p>
  </div>
</template>
<script>



export default {
  name: 'App',
  data(){
    return{
      products: ['역삼동원룸', '천호동원룸', '마포구원룸'],
      menuitems: ['home', 'about', 'products'],
      bbippo: 0,
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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
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
