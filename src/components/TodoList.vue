<template>
    <h1>Hello from TODO List template</h1>
</template>

<script>
export default {
    data(){
        return {
            todos: [
                {todoString: "Make Angular course", completed:false},
                {todoString: "Cook Some Food", completed:true},
                {todoString: "See youtube videos", completed:true},
                {todoString: "Publish these videos", completed:false},
            ]
        }
    },
    methods: {
        addTodo(newTodo){
            this.todos.push({
                todoString: newTodo,completed:false
            })
        },
        toggleTodo(todo){
            todo.completed = !todo.completed;
        },
        editTodo(todo, newTodoString){
            todo.todoString = newTodoString;
        },
        deleteTodo(deleteTodo){
            this.todos = this.todos.filter( todo => todo !== deleteTodo )
        }
    }
}
</script>


<style>

</style>