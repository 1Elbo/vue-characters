<template>
    <form @submit.prevent="formSubmitted">
    <input type="text" required="true" placeholder="Add character here" @input="valueChanged" v-model="newChar"/><br>
    <button class="button-30" role="button" >Add Character</button>
  </form>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

</style>