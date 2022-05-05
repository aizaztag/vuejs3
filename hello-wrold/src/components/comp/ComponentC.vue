<template>
    <div>
      Compoent C 
      <ComponentE></ComponentE>
    </div>
</template>

<script>
    import ComponentE  from './ComponentE.vue'
    export default {
        components : {ComponentE},
        name : 'ComponentC',
      
    }
</script>

<style lang="scss" scoped>

</style>