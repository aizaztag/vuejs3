<template>
    <div>
       Compoent E
       <ComponentF></ComponentF>
    </div>
</template>

<script>
    import ComponentF  from './ComponentF.vue' 
    export default {
        components : {ComponentF},
        name : 'ComponentE'
        
    }
</script>

<style lang="scss" scoped>

</style>