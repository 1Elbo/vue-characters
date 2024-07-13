<template>
    
    {{ name }}
      <div class="cross" @click="returnIndex">
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
            id:{
                type: Number
            }
        },
        methods: {
            returnIndex() {
               /* this.$emit("return-index", id )  */
               this.$emit("return-index", this.id)
               
               
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>