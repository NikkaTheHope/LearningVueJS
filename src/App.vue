<template>
  <nav class="menu">
    <a v-for="menu in menus" :key="menu">{{ menu }}</a>
  </nav>  
  <img alt="Vue logo" src="./assets/logo.png" />
  <p>{{logo}}</p>
  <div v-for="(product,i) in products" :key="product">
    <h4 :style="스타일">{{product}}</h4>
    <p>{{ price1 }} 만원</p>
    <button @click="warns[i]++">매물신고버튼</button> <span> 신고 수 : {{warns[i]}} </span>
  </div>

</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      price1: 60,
      price2: 70,
      logo: `원룸샵`,
      스타일: `color: blue;`,
      products : ["역삼동원룸","천호동원룸","마포구원룸"],
      menus : ["Home","Products","About"],
      warns: [0,0,0]
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
  margin-top: 60px;
}
button{
  background: rgb(110, 213, 156);
  color: darkgreen;
  padding: 7px;
  border-radius: 10px;
}
button:hover{
  background: white;
}
button:active{
  transform: scale(0.9);
}
.menu{
  background: rgb(110, 213, 156);
  padding: 10px;
  border-radius: 20px;
}
.menu a{
  text-decoration: none;
  color: darkgreen;
  padding: 20px;
}
</style>
