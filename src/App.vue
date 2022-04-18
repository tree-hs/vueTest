<template>
  <div>
    <div class="menu">
      <a v-for="(a,i) in menus" :key="i" href="">{{a}}({{i}})</a>
    </div>
    <div>
      <h4 class="red" :style="스타일">XX 원룸</h4>
      <p>{{ price1 }} 만원</p>
    </div>
    <div style="border:1px solid #ddd;">
      <h4 v-for="(a,i) in product2" :key="i">{{a}}({{i}})</h4>
    </div>
    <div>
      <h4>{{products[0]}}</h4>
      <h4>{{products[1]}}</h4>
      <h4>{{products[2]}}</h4>
      <p>{{ price2 }} 만원</p>
    </div>

    <div class="class-two">
      <button @click="신고수 += 1">허위매물신고</button><span>신고횟수 : {{신고수}}건</span><br/>
      <button @click="increase">매물추천</button><span>추천횟수 : {{추천수}}건</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      price1 : 80,
      price2 : 70,
      스타일 : "color : blue",
      menus : ['Home','Shop','About'],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      product2 : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      신고수 : 0,
      추천수 : 0,
    }
  },
  methods : {
    increase(){
      this.추천수 += 1;
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


.menu {
  background-color:darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color:#fff;
  padding: 10px;
  text-decoration: none;
}
</style>
