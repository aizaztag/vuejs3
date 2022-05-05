<template>
<div>
    <h2 v-if="num === 0">Here</h2>
    <h2 v-else-if="num < 0">Negative number</h2>
    <h2 v-else>not 5</h2>

    <template  v-if="display === true">
        <h2>One</h2>
        <h2>Two</h2>
        <h2>Three</h2>
    </template>

    <h2 v-show="show">HOw or hide</h2>
    

   </div> 

</template>

<script>

export default {
 name :'Rendering',
 data(){
    return{
        num:-2,
        display:true,
        show:false,
    }    
 }
}
</script>
