<template>
  <div id="id">
      <TodoHeader></TodoHeader>
      <TodoInput @addTodo="addTodo"></TodoInput>
      <TodoList :propsdata="todoItems"></TodoList>
      <TodoFoot @removeAll="clearAll"></TodoFoot>
  </div>
</template>

<script>
import TodoHeader from './components/TodoHeader.vue'
import TodoInput from './components/TodoInput.vue'
import TodoList from './components/TodoList.vue'
import TodoFoot from './components/TodoFoot.vue'

export default {
  components: {
    'TodoHeader' : TodoHeader,
    'TodoInput' : TodoInput,
    'TodoList' : TodoList,
    'TodoFoot' : TodoFoot,  
  },
  data() {
      return{
          todoItems: []
      }
  },
  created() {
      for(var i = 0; i < localStorage.length; i++){
          this.todoItems.push(localStorage.key(i));
      }
  },
  methods: {
    addTodo(todoItem) {
      localStorage.setItem(todoItem, todoItem);
      this.todoItems.push(todoItem);
    },
    clearAll() {
      localStorage.clear();
      this.todoItems = [];
    }
  }
}
</script>

<style>
   body {
        text-align: center;
        background-color: #F6F6F8;
    }

</style>
