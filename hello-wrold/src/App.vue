<template>
<div  :id="id">
  {{name}}
  <button :disabled="isDisabled">Bind</button>
  <h2 :class="status">Bind</h2>
  <h2 :class="isPromoted && 'promoted'">Italic</h2>
  <h2 :class="isSoldOut ? 'sold-out' : 'new'">Sold or new</h2>
  <h2 :class="['new' , 'promoted']">new or promoted</h2>
   array class  
  <h2 :class="[isPromoted && 'promoted' , isSoldOut ? 'sold-out' : 'new']"> array conditional new or promoted</h2>
  object class
  <h2 :class="{
      promoted: isPromoted,
      'sold-out': isSoldOut,
      new: ! isSoldOut
    }"
   > 
  array conditional new or promoted</h2>

     object Style
   <h2 :style="{
          color: hightlightColor,
          'font-style': fontStyle,
          fontSize: fontStyle + 'px',
   }">
     Font Style
   </h2>


     object Style
   <h2 :style="styleObject">
     Font Style Object
   </h2>

    <div :style="[styleBase , styleSuccess]">
        array style class
    </div>

</div>

  
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      name  : "'<b>Aizaz</b>'",
      id  : "3",
      isDisabled:false,
      status:'underline',
      isPromoted:true,
      isSoldOut:false,
      hightlightColor:'Orange',
      fontStyle:'50',
      styleObject:{
        color:'red',
        fontSize:'60px'
      },
       styleBase:{
        color:'green',
        fontSize:'60px'
      },
       styleSuccess:{
        fontStyle:'italic',
        padding:'60px'
      }
    }
  }
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.underline{
  text-decoration: underline;
}

.promoted{
  font-style: italic;
}

.new{
  color: green;
}

.sold-out{
  color: red;
}
</style>
