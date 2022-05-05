<template>
    <div class="">
        {{ volume }}
        <button  @click="volume += 2">Up volume</button>  
        <button  @click="volume -= 2">Down volume</button>  
        <input type="text" v-model="movie" />  
        <input type="text" v-model="movieInfo.title" />  
        <input type="text" v-model="movieInfo.actor" />  
    </div>
</template>

<script>

export default {
    name : 'watch',
    data() {
        return{
          volume  : 0,
          movie  : '',
          movieInfo  : {
              title : '',
              actor : ''
          }
        }
    },
    watch:{
        volume(newValue , oldValue){
            if(newValue > oldValue && newValue === 20){
                alert('toe loud');
            }
        },
        movie:{
            handler(newValue){
                console.log('movie handler');
            },
            immediate : true // call on page load
        },
        movieInfo:{
            handler(newValue){
                console.log('nested object property ' +   `${newValue.title} ${newValue.actor}`);
            },
            deep : true // nested object property
        }
    }
}
</script>
