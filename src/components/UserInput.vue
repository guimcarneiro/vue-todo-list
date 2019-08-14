<template>
    <div id="userInputContainer">
        <input v-model="text" placeholder="Digite uma todo" />
        <button v-on:click="submitted">Enviar</button>
    </div>
</template>

<script>
export default {
    name: 'UserInput',
    data: function() {
        return {
            text: ''
        }
    },
    methods: {
        submitted: function () {
            this.$emit('userInputSubmit', this.text);
        }
    }
}
</script>

<style scoped>

</style>