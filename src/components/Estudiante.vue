<template>
  <div class="container">
    <label for="id_nombre">Nombre</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text"/>
    
    <label for="id_apellido">Apellido</label>
    <input v-model="nuevoApellido" id="id_apellido" type="text"/>
    <button v-on:click="agregarEstudiante">Agregar Edtudiante</button>
    {{ nuevoNombre }}
    <ul>
      <li v-for="{nombre, apellido} in lista" :key="nombre">
        Nombre: {{nombre}} - Apellido: {{apellido}} 
     </li>
    </ul>
  </div>
</template>
 
<script>
export default {
  data() {
    return {
        nuevoNombre:"Nuevo",
      lista: [
        { nombre: "Belen", apellido: "Paca" },
        { nombre: "Josefina", apellido: "Paca" },
        { nombre: "Andy", apellido: "Cueva" },
        { nombre: "Paul", apellido: "Esponja" },
        { nombre: "Camila", apellido: "Est" },
        { nombre: "Carla", apellido: "Mardo" },
        { nombre: "Anahis", apellido: "Silva" },
      ],
    };
  },
  methods:{
    agregarEstudiante(){
        const nuevo={
            nombre: this.nuevoNombre,
            apellido: this.nuevoApellido,
        };
        // this.lista.unshift(nuevo);
        this.lista.push(nuevo);

    },

  },
};
</script>
 
<style>
li {
  font-size: 20px;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}
</style>