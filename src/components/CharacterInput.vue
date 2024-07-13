<template>
    <form @submit.prevent="addNewCharacter">
    <input type="text" required="true" placeholder="Add character here" v-model="newChar"/><br>
    <button class="button-30" role="button" >Add Character</button>
  </form>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>

</style>