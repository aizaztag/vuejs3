<template>
    <div>
       Component F injecting data property from parent compoent to nested tree component here  {{username}}
    </div>
</template>

<script>
    export default {
        name : 'ComponentF',
          inject:['username']
    }
</script>

<style lang="scss" scoped>

</style>