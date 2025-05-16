<template>
  <div class="container">
    <label for="id_nombre">Nombre:</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />
       <label for="id_apellido">Nombre:</label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />
    <button v-on:click="agregarEstudiante()">Agregar Estudiante</button>
    {{ nuevoNombre }}
    <ul>
      <li v-for="{ nombre, apellido } in lista" :key="nombre">
        Nombre: {{ nombre }} - Apellido: {{ apellido }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nuevoNombre: "execuitor",
      lista: [
        { nombre: "Erick", apellido: "Enriquez" },
        { nombre: "danilo", apellido: "parrales" },
        { nombre: "carlos", apellido: "segovia" },
        { nombre: "jessica", apellido: "teran" },
        { nombre: "ana", apellido: "castillo" },
      ],
    };
  },
  methods: {
    agregarEstudiante() {
        const nuevo={
            nombre:this.nuevoNombre,
            apellido:'Enriquez',
        }
        /*this.lista.unshift(nuevo);*/
        this.lista.push(nuevo);
    },
  },
};
</script>

<style>
</style>