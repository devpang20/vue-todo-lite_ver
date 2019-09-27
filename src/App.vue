<template>
  <div id="id">
      <TodoHeader></TodoHeader>
      <TodoInput></TodoInput>
      <TodoList></TodoList>
      <TodoFoot></TodoFoot>
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
 }
}
</script>

<style>
   body {
        text-align: center;
        background-color: #F6F6F8;
    }

</style>
