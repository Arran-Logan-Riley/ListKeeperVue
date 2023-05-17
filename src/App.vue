<template>
  <div>
    <todo-list :msg="titleProp"></todo-list>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'

export default {
  components:{
    //Import the toDoList component
    TodoList
  },
  //Define the data object to save an isntance of the components data
  data(){
    return{
      titleProp: 'To do list'
    }
    
  }
};
</script>