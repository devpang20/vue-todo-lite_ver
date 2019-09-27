<template>
  <div id="app">
      <span @click="clearTodo">비우기</span>
  </div>
</template>

<script>
export default {
    methods: {
     clearTodo(){
            this.$emit('removeAll'); 
        }
    }
}
</script>

<style>

</style>
