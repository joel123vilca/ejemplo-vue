<template>
  <div id="app" class="container">
    <div class="jumbotron">
      <titulo :titulo="titulo"></titulo>
      <nueva-tarea v-bind:tareas="tareas"></nueva-tarea>
    </div>
  </div>
</template>

<script>
import Titulo from './TituloComponent.vue'
import NuevaTarea from './NuevaTareaComponent.vue'
export default {
  components: {
    Titulo,
    NuevaTarea
  },
  data(){
    return{
      titulo: 'Lista de tareas',
      tareas:[
        {
          texto: 'Aprender Vue.js',
          terminada: false
        },
        {
          texto: 'Aprender React.js',
          terminada: false
        },
        {
          texto: 'Aprender React Native',
          terminada: false
        }
      ]
    }
  }
}

</script>

<style>


</style>
