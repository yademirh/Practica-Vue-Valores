<script setup>
  import { ref, computed } from 'vue'; 


  const users = [
    {
      name: 'Pepito',
      lastame: 'Perez'
    },
    {
      name: 'Jane',
      lastame: 'Doe',
      age: 30
    }
  ]

  var num = ref(0);
  const msg = "ASASA";
  console.log(msg);

  num.value = 3;

  const computado = computed(function() {
    if(num.value>0){
     return num.value*2;
    }else{
      // num.value = 0;
    }
    return (0);
  }) 
  // const mostrar = () => {
  //   alert("me están llamando");
  // }

  // const mostrar = function() {
  //   alert("me están llamando");
  // }

  function mostrar () {
    console.log("me están llamando");
  }

</script>
///////////////////////////////////////////////////////////////////////////////////////
<template>

  <div id="cuadros">
    <h1>Holaaa {{ msg }}</h1>
    <h1>Valor {{ num }}</h1>
    {{ mostrar() }}
    <h1>Valor computado {{ computado }}</h1>
  </div>

  <div v-for="(user, index) in users" :key="index">
    Nombre Completo: {{ user.name }} {{ user.lastame }}<br>
    <span v-if="user.age">
      Edad: {{ user.age }}
    </span>
  </div>

</template>
///////////////////////////////////////////////////////////////////////////////////////
<style scoped>
#cuadros{
  display: flex;
  width: 50%;
  /* flex-direction: column; */
  justify-content: space-around;
  align-items: center;
  margin: auto 0;
  background-color: #ededed;
}
  h1{
    color: blue;
    width: 200px;
    height: 100px;
    background-color: chartreuse;
    display: flex;
    text-align: center;
    align-items: center;
    justify-content: center;
    outline: 3px solid black;
    transition: all .5s;
  }
  h1:hover{
    background-color: aqua;
    color: black;
    box-shadow: 0 0 10px black;
    transition: all .5s;
    
  }
</style>
