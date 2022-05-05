<template>
    <div>
          <h2>This is a popup</h2>
          <button @click="$emit('close')">Close Popup</button>
    </div>
</template>

<script>
    export default {
        name :  'PopUP',
        emits : ['close']
    }
</script>

<style lang="scss" scoped>

</style>