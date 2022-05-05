<template>
    <div>
        <h2>TabC</h2>
        <input type="text" :v-model="name" />
    </div>
</template>

<script>
import Input from '../Input.vue'
    export default {
  components: { Input },
        name  : "TabC",
        data(){
            return{
                name : ''
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>