<template>
    <div>
        <h1> This component is a child </h1>
        <input type="text" placeholder="Input a text to pass to a page" v-model="text">
        <button @click="sendTopage"> Send to page </button>
        <h1> End of child </h1>
        <hr>
    </div>
</template>

<script>
export default{
    data() {
        return {
            text: "",
        }
    },
    methods: {
        sendTopage() {
            this.$emit('sendTopage', this.text)
        }
    }
}
</script>

<style scoped>

</style>
