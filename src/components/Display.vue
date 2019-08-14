<template>
    <div id="display">
        <ul>
            <li v-for="todo in todos" v-bind:key="todo.id">{{ todo.text }}</li>
        </ul>
        <UserInput v-on:userInputSubmit="handleSubmitTodo"></UserInput>
    </div>
</template>

<script>
  import UserInput from './UserInput.vue';

export default {
    name: 'TodosDisplay',
    components: {
        UserInput
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
        }
    }
}
</script>

<style>
    #display li{
        list-style-type: none;
    }
</style>