<template>
<div>
    <div v-for="data in Json" :key="data.name" class="card">    
 
      <img :src="data.avatar_url" alt="Default" height="100px" width="100px">
  
      <div class="container">
      <h4><b>{{data.name}}</b></h4> 
      <a :href="data.github_url">{{data.github_url}} </a> 
      <p>{{data.nickName}}</p> 
      </div>      
    </div>
    </div>
</template>

<script>
import json from './data.json'
export default {
  name: 'HelloWorld',
  data(){
    return{
      Json: json.users
    }
  },
  props: {
    msg: String
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}
.container {
  padding: 2px 16px;
}
.card {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  border-radius: 5px; 
  margin: 50px;
}
img {
  border-radius: 5px 5px 0 0;
}
</style>
