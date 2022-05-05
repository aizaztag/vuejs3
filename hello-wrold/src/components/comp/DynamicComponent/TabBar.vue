<template>
    <div>
        <button @click="$emit('activeTab' , 'TabA')">Tab A</button>
        <button @click="$emit('activeTab' , 'TabB')">Tab B</button>
        <button @click="$emit('activeTab' , 'TabC')">Tab C</button>
        <keep-alive>
          <component :is="activeTab" /> 
        </keep-alive>
    <!-- <TabA v-if="activeTab === 'TabA'"></TabA>
    <TabB v-if="activeTab === 'TabB'"></TabB>
    <TabC v-if="activeTab === 'TabC'"></TabC> -->
     </div>
</template>

<script>
    import TabA from  './TabA.vue'
    import TabB from  './TabB.vue'
    import TabC from  './TabC.vue'
    export default {
        name  : "TabBar",
        components : {TabA , TabB , TabC },
        props : ['activeTab'],
        emits : ['activeTab']
    }
</script>

<style lang="scss" scoped>

</style>