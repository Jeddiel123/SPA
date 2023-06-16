<script>
import axios from 'axios'
export default {
  data() {
    return {
      nombre: "",
      edad:"",
      estadocivil:"",
      trabajo:"",
      residencia:"",
      cita:"",
      citaAutor:"",
      bio:"",
      personalidad01:"",
      personalidad02:"",
      personalidad03:"",
      personalidad04:"",
      objetivos:[],
      frustaciones:[],
      motivaciones:[],
      marcas:[]
    }
  },
  methods: {
submit(){
axios
.post("/api/guardarPersonasUxd.php", {
nombre: this.nombre,
edad: this.edad,
estadoCivil: this.estadocivil,
trabajo: this.trabajo,
residencia: this.residencia,
cita: this.cita,
citaAutor: this.cita,
bio: this.bio,
personalida01: this.personalidad1,
personalidad02: this.personalidad2,
personalidad03: this.personalidad3,
personalidad04: this.personalidad4,
objetivos:this.objetivos,
frustraciones: this.frustraciones,
motivaciones: this.motivaciones,
marcas: this.marcas,
//completar las variables, estas deben llamarse como las que se recibirán en el backend sin el símbolo del dolar $
})
.then((response) => {
console.log(response.status)
})
  },
},
}
</script>
<template>
<div class="grid grid-cols-4 p-2 m-5">
    <div>
      <label for="nombre"> Nombre </label>
      <br />
      <input
        v-model="nombre"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>

    <div>
      <label for="edad"> Edad </label>
      <br />
      <input
        v-model="edad"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="number"
      />
    </div>

    <div>
      <label for="estadoCivil"> Estado Civil </label>
      <br />
      <input
        v-model="estadoCivil"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="estadoCivil"
      />
    </div>

    <div>
      <label for="trabajo"> Trabajo </label>
      <br />
      <input
        v-model="trabajo"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>

    <div>
      <label for="residencia"> Residencia </label>
      <br />
      <input
        v-model="residencia"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>

    <div>
      <label for="cita"> Cita </label>
      <br />
      <input
        v-model="cita"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>

    <div>
      <label for="citaAutor"> Autor de la cita </label>
      <br />
      <input
        v-model="citaAutor"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>

    <div>
      <label for="bio"> Biografia </label>
      <br />
      <input
        v-model="bio"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>
    <div>
      <label for="personalidad01"> Personalidad 1</label>
      <br />
      <input
        v-model="personalidad01"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>
    <div>
      <label for="personalidad02"> Personalidad 2</label>
      <br />
      <input
        v-model="personalidad02"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>
    <div>
      <label for="personalidad03"> Personalidad 3</label>
      <br />
      <input
        v-model="personalidad03"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>
    <div>
      <label for="personalidad04"> Personalidad 4</label>
      <br />
      <input
        v-model="personalidad04"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>

    <div>
      <label for="objetivos"> Objetivos </label>
      <br />
      <input
        v-model="objetivos"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>

    <div>
      <label for="frustraciones"> Frustraciones </label>
      <br />
      <input
        v-model="frustraciones"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>

    <div class="card">
      <label for="motivaciones"> Motivaciones </label>
      <br />
      <input
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
      <br />
      <label
        for="default-range"
        class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
        >Porcentaje</label
      >
      <input
        v-model="porcentaje"
        id="default-range"
        type="range"
        class="w-48 h-2 bg-gray-200 rounded-lg appearance-none cursor-pointer dark:bg-gray-700"
      />
    </div>

    <div>
      <label for="marcas"> Marcas </label>
      <br />
      <input
        v-model="marcas"
        class="shadow appearance-none border rounded-full w-48 p-1 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
      />
    </div>
  </div>
  <button
    class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
    @click=" submit()"
  >
    Submit
  </button>
</template>