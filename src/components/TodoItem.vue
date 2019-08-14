<template>
  <div id="todo">
      <div>
        <h3>{{ text }}</h3>
      </div>
      <div>
          <button v-on:click='clickDeleteItem'>Deletar</button>
      </div>
  </div>
</template>

<script>
export default {
    name: 'TodoItem',
    props:{
        text: String
    },
    methods: {
        clickDeleteItem: function() {
            this.$emit('clickDeleteItem');
        }
    }
}
</script>

<style>
    #todo {
        border: 1px solid black;
    }
</style>