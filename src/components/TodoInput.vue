<template>
  <div id="app">
      <input type="text" v-model="newTodoItem">
      <button @click="addTodo">등록</button>
  </div>
</template>

<script>
export default {
        data(){
            return{
                newTodoItem: ''
            }
        },
        methods: {
            addTodo(){
                localStorage.setItem(this.newTodoItem, this.newTodoItem)    
                this.clearInput();
            },
            clearInput(){ 
                this.newTodoItem = '';
            }
        }

}
</script>

<style>

</style>
