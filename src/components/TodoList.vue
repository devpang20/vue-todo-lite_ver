<template>
    <section>
        <ul>
            <li v-for="(todoItem, index) in todoItems" :key="todoItem">{{todoItem}}
                <span type="button" @click= "removeTodo(todoItem, index)" >
                        삭제
                </span>
            </li>
        </ul>
    </section>
</template>
<script>
export default {
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
        removeTodo(todoItem, index){
            localStorage.removeItem(todoItem);
            this.todoItems.splice(index, 1);
        }
    }
}
</script>

<style>

</style>
