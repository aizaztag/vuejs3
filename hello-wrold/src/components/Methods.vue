<template>
    <div>
   
    <button @click="add() , increment(3 , $event)">Click to change the name {{base}} </button>
    <button @click="increment(3 , $event) ">increament 3 </button>
    {{counter}}
    </div>
</template>

<script>

export default{
    data() {
        return{
           base : 3,
           num : 3,
           name : 'dfsdf',
           counter : 2,
        }
    },
     methods:{
            add () {
             return this.base  =  2;
            },
            increment (num , event) {
                console.log('ere' , event)
             return this.counter +=num;
            }
        }
}
</script>
