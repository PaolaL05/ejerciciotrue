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

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
</style>
