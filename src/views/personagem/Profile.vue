<template>
<div>
  <div v-if="false">
      <h1>perfil</h1>
     <pre> {{ bio }} </pre>
</div>

  <div v-show="false"> 
    Nao tenho dado para ser exibido!
  </div>

  <div v-if="isStatus">
     {{showFullName}} <br>
      {{setName}} <br>
      {{setFruit}}


      <ul v-for="fruit in setFruit" :key="fruit.id">
           <li> {{fruit}}</li>
      </ul>
  </div>
</div>

</template>
<script>
export default {
    name: 'Perfil',
    data() {
        return{
            name: 'Alex',
            lastname: 'Salvador',
            isStatus : true,
            bio: {
                name: 'Juao',
                bio: 'Hooola',
                photo:'',
                power:'trovao',
                enemies:'nuvem',
                weaks:'dia ensolarado',
                status: false,
            }  
        }
    },

    computed: {
        showFullName(){
            return this.name + " " + this.lastname;
        },
        setName() {
            this.name = 'Zé lelé';
            return this.name;
        },
        setFruit() {
            const fruits = ['abacate', 'limao'];
            return fruits;
        },
    },


};
</script>