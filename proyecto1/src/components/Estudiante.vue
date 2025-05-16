<template>
  <div class="container">
    <label for="id_nombre">Nombre:</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />
       <label for="id_apellido">Apellido:</label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />
     <label for="id_edad">Edad:</label>
    <input v-model="nuevoEdad" id="id_edad" type="text" />
      <label for="id_nacional">nacionalidad:</label>
    <input v-model="nuevoNacionalidad" id="id_nacional" type="text" />
      <label for="id_cedula">cedula:</label>
    <input v-model="nuevoCedula" id="id_cedula" type="text" />
    
    <button v-on:click="agregarEstudiante()">Agregar Estudiante</button>
    {{ nuevoNombre }}
    <ul>
      <li v-for="{ nombre, apellido, edad, nacionalidad, cedula } in lista" :key="nombre">
        Nombre: {{ nombre }} - Apellido: {{ apellido }} - Edad:{{ edad }} - nacionalidad:{{ nacionalidad }} - Cedula:{{ cedula }}
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
            apellido:this.nuevoApellido,
            edad: this.nuevoEdad,
            nacionalidad:this.nuevoNacionalidad,
            cedula: this.nuevoCedula,
        }
        /*this.lista.unshift(nuevo);*/
        this.lista.push(nuevo);
    },
  },
};
</script>

<style>
</style>