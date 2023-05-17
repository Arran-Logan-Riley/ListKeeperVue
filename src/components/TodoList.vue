<template>
    <div>
      <h1>To-Do List</h1>
      <input v-model="newTodo" type="text" placeholder="Add a new task">
      <button @click="addTodo">ADD</button>
      <ul>
        <li v-for="(todo, index) in todos"
        :key="index"
        >{{ todo }}
        <button @click="removeTodo(index)">Remove</button>
      </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data(){
      return {
        todos:[],
        newTodos: ''
      };
    },
    methods:{
      addTodo(){
        //newTodo is the text field. 
        if(this.newTodo.trim() !== ''){
          this.todos.push(this.newTodo);
          this.newTodo = '';
        }
      },
      removeTodo(index){
        this.todos.splice(index, 1)
      }
    }
  }
  </script>