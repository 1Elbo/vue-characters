<template>
    
    {{ name }}
      <div class="cross" @click="removeCharacter">
        <div class="bar1"></div>
        <div class="bar2"></div>
      </div>
    
</template>

<script>
    export default {
        props: {
            name: {
                type: String
            },
        },
    }
</script>

<style lang="scss" scoped>

</style>