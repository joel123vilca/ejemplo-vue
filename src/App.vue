<template>
  <div id="app" class="container">
    <div class="jumbotron">
      <titulo :titulo="titulo"></titulo>
      <nueva-tarea v-bind:tareas="tareas"
        :actualizarContador="actualizarContador"></nueva-tarea>
      <lista-tareas :tareas="tareas"></lista-tareas>
    </div>
  </div>
</template>

<script>
import Titulo from './TituloComponent.vue'
import NuevaTarea from './NuevaTareaComponent.vue'
import ListaTareas from './ListaTareasComponent.vue'

export default {
  components: {
    Titulo,
    NuevaTarea,
    ListaTareas
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
  },
  methods: {
    actualizarContador(){
      this.numTareas++;
    }
  }
}

</script>

<style>


</style>
