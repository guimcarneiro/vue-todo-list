<template>
    <div id="display">
        <ul>
            <TodoItem 
                v-for="todo in todos" 
                v-bind:key="todo.id" 
                v-bind:text="todo.text" 
                v-on:clickDeleteItem="handleDeleteTodo(todo.id)"></TodoItem>
        </ul>
        <UserInput v-on:userInputSubmit="handleSubmitTodo"></UserInput>
    </div>
</template>

<script>
  import UserInput from './UserInput.vue';
  import TodoItem from './TodoItem.vue';

export default {
    name: 'TodosDisplay',
    components: {
        UserInput,
        TodoItem
    },
    data: function() {
        return {
            todos: []
        }
    },
    methods: {
        handleSubmitTodo: function(text) {
            this.todos.push({
                id: this.todos.length,
                text
            })
        },
        handleDeleteTodo: function(id) {
            this.todos.splice(id, 1);
        }
    }
}
</script>

<style>
    #display li{
        list-style-type: none;
    }
</style>