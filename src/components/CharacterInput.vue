<template>
    <form @submit.prevent="formSubmitted">
    <input type="text" required="true" placeholder="Add character here" @input="valueChanged" v-model="newChar"/><br>
    <button class="button-30" role="button" >Add Character</button>
  </form>
</template>

<script>
    export default {
        data() {
            return {
                newChar: ""
            }
        },
        methods: {
            formSubmitted() {
                console.log(this.newChar)
                this.$emit("add-character", this.newChar)
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>