<template>
    <section>
        <ul>
            <li v-for="(todoItem, index) in propsdata" :key="todoItem">
                {{todoItem}}
                <span type="button" @click= "removeTodo(todoItem, index)" >
                        삭제
                </span>
            </li>
        </ul>
    </section>
</template>
<script>
export default {
    props:['propsdata'],
    methods: {
        removeTodo(todoItem, index){
            this.$emit('removeTodo', todoItem, index);
       }
    }
}
</script>

<style>

</style>
