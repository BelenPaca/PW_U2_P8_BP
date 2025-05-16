<template>
  <div class="container">
    <label for="id_nombre">Nombre</label>
    <input v-model="nuevoNombre" id="id_nombre" type="text" />

    <label for="id_apellido">Apellido</label>
    <input v-model="nuevoApellido" id="id_apellido" type="text" />

    <label for="id_genero">Género</label>
    <input v-model="nuevoGenero" id="id_genero" type="text" />

    <label for="id_edad">Edad</label>
    <input v-model="nuevaEdad" id="id_edad" type="number" />

    <label for="id_correo">Correo</label>
    <input v-model="nuevoCorreo" id="id_correo" type="email" />

    <button v-on:click="agregarEstudiante">Agregar Edtudiante</button>
    {{ nuevoNombre }}
    <ul>
      <li v-for="{ nombre, apellido, genero, edad, correo } in lista" :key="nombre + apellido">
        Nombre: {{ nombre }} - Apellido: {{ apellido }} - Género: {{ genero }} - Edad: {{ edad }} - Correo: {{ correo }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nuevoNombre: "Nuevo",
      nuevoApellido: "Nuevo",
      nuevoGenero: "Nuevo",
      nuevaEdad: null,
      nuevoCorreo: "Nuevo",
      lista: [
        { nombre: "Belen", apellido: "Paca", genero: "F", edad: 20, correo: "belen@gmail.com"},
        { nombre: "Josefina", apellido: "Perez", genero: "F", edad: 22, correo: "josefina@gmail.com"},
        { nombre: "Andy", apellido: "Cueva", genero: "M", edad: 23, correo: "andy@gmail.com"},
        { nombre: "Paul", apellido: "Freire", genero: "M", edad: 24, correo: "paul@gmail.com"},
        { nombre: "Camila", apellido: "Serrano", genero: "F", edad: 25, correo: "camila@gmail.com"},
        { nombre: "Carla", apellido: "Lopez", genero: "F", edad: 26, correo: "carla@gmail.com"},
        { nombre: "Anahis", apellido: "Silva", genero: "F", edad: 27, correo: "anahis@gmail.com"},
      ],
    };
  },
  methods: {
    agregarEstudiante() {
      const nuevo = {
        nombre: this.nuevoNombre,
        apellido: this.nuevoApellido,
        genero: this.nuevoGenero,
        edad: this.nuevaEdad,
        correo: this.nuevoCorreo,
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