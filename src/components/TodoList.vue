<template>
    <div>
      <h1>{{ msg }}</h1>
      <input v-model="newTodo" type="text" placeholder="Add a new task">
      <button @click="addTodo">ADD</button>
      <ul>
        <!--Use the vue-for to automatically loop the creation of the list items [List, Key]-->
        <li v-for="(todo, index) in todos"
        :key="index"
        >:{{ index }} {{ todo }} 
        <button @click="removeTodo(index)">Remove</button>
      </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    //make sure that when you send props that you accespt the props as a
    //data type
    props: {
    msg: String
  },
  //define the default data object
    data(){
      return {
        todos:[],
        newTodos: ''
      };
    },
    methods:{
      addTodo(){
        //newTodo is the text field. .trim() removes white space from each side of the string
        if(this.newTodo.trim() !== ''){
          this.todos.push(this.newTodo);
          this.newTodo = '';
        }else{
            alert('No data was entered');
        }
      },
      removeTodo(index){
        //access the todos list and remove a item via the index
        this.todos.splice(index, 1)
      }
    }
  }
  </script>