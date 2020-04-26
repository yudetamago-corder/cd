<template>
  <div class="home">
    <table>
      <tr><th>学習年</th><th>学習開始日</th><th>学習言語</th></tr>
      <tr><td>{{estra.name}}</td><td>{{estra.day}}</td><td>{{estra.la}}</td></tr>
      <tr><td>{{inc.name}}</td><td>{{inc.day}}</td><td>{{inc.la}}</td></tr>
      <tr><td>{{window.name}}</td><td>{{window.day}}</td><td>{{window.la}}</td></tr>
    </table>
    <h1>今日やる事</h1>
    <ul>
      <li v-for="data in todos" :key="data.key">{{todo}}</li>
    </ul>
    <input type="text" v-model="newTodo">
    <input type="submit" value="add" @click="addTodo()">
  </div>
</template>
<script>
  export default{
    data(){
      return{
        newTodo:"",
        todos:[
          "起床"
        ],
        estra:{
          name:"2017",
          day:"3月2日",
          la:"html"
        },
        inc:{
          name:"2019",
          day:"5月24日",
          la:"vue.js"
        },
        window:{
          name:"2016",
          day:"3月19日",
          la:"php"
        }
      }
    },
    methods:{
      addTodo(){
          this.todos.push(this.newTodo);
          this.newTodo="";
      }
    }

  }
</script>
<style scoped>
 th{
   width:20%;
   background:#e6e6e6;
 }
 td{
   width:20%;
   background:#f2f2f2;
 }
 {
   color: red;
 }
 </style>