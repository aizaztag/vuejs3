<template>
<div class="">
    Expmple 1
     <br>
    property {{ firstName}}  {{ lastName}}
    <br>
    Computed property  {{ fullName}}  
     <br>
     <button @click="changeFullName">Change changeFullName</button>
    Expmple 2
     <br>
    property {{  cart.reduce((total , curr) => ( total += curr.price) , 0) }} 
     <br>
    Computed property  {{ total}} 
    <br>
      
    change property  <button @click="items.push({id:1 , price:30})">Add price 30</button>
    <br>

    v for and v if without computed property
     <br>
    <template v-for="item in items" :key="item.id">
        <h2 v-if="item.price > 100">{{ item.price }}</h2>
    </template>
    v for using computer property
     <h2 v-for="item in getExpensiveItem" :key="item.id">
         {{  item.price }}
    </h2>

</div>
</template>

<script>


export default {
    data() {
        return {
             firstName : 'Aizaz',
             lastName : 'Aizaz',
             items : [
                 {
                   id:1,
                   price  : 100
                 },
                 {
                   id:2,
                   price  : 300
                 },
                 {
                   id:3,
                   price  : 200
                 },
             ], 
             cart : [
                 {
                   id:1,
                   price  : 200
                 },
                 {
                   id:2,
                   price  : 300
                 },
                 {
                   id:3,
                   price  : 200
                 },
             ]
        }
    },
    methods:{
      changeFullName(){
          return this.fullName = 'New Name';
      }
    },
    computed:{
        fullName:{
           get(){
             return  `${this.firstName} ${this.lastName}`
           },
           set(value){
              const names = value.split(' ')
              this.firstName =  names[0];
              this.lastName =  names[1];
           },
        },
        total(){
            return   this.items.reduce((total , curr) => ( total += curr.price) , 0)
        },
        getExpensiveItem(){
            return this.items.filter(item  => item.price >  100 )
        }
    }
}
</script>
