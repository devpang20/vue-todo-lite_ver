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
                var value = this.newTodoItem;
                console.log(value);
                this.$emit('addTodo',value);
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
