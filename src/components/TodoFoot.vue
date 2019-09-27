<template>
  <div id="app">
      <span @click="clearTodo">비우기</span>
  </div>
</template>

<script>
export default {
    methods: {
     clearTodo(){
            localStorage.clear(); 
        }
    }
}
</script>

<style>

</style>
