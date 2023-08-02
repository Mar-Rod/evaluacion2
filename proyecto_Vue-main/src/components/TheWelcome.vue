<script setup>
// Variable reactiva
import { ref} from 'vue'

const registro = ref({
  nombre: '',
  apellido: '',
  genero: '',
  edad: '',
  email: '',
  password: '',
  opciones: [],
  administrador: false,
  observaciones: '',
  grupo: ''
})

const guardar = (e) => {
  e.preventDefault();
  console.log(registro.value);
  cambio.value=false
}

const restablecer = (e) => {
  e.preventDefault();
  //Limpiar los campos
  nombre.value = '';
  apellido.value = '';
  edad.value = '';
  email.value = '';
  password.value = '';
  observaciones.value = '';
  grupo.value = '';
}

let cambio = ref(true)
</script>

<template>
  <WelcomeItem>
    
    <template ></template>
    <form>
      <label for="nombre">
      Nombre:
      <br>
      <input type="text" id="nombre" v-model="registro.nombre">
    </label>
    <br>
    <label for="apellido">
      Apellido:
      <br>
      <input type="text" id="apellido" v-model="registro.apellido">
    </label>
    <br>
    <label >
      <strong>Género:</strong>
      <br>
      <label for="g-masculino">Masculino<input type="radio" id="g-masculino" name="genero" value="m" v-model="registro.genero"></label>
      <label for="g-femenino">Femenino<input type="radio" id="g-femenino" name="genero" value="f" v-model="registro.genero"></label>
    </label>
    <br>
    <label for="edad">
      Edad
      <br>
      <input type="number" id="edad" max="100" min="16" v-model="registro.edad">
    </label>
    <br>
    <label for="email">
      Correo:
      <br>
      <input type="email" id="email" v-model="registro.email">
    </label>
    <br>
    <label for="password">
      Contraseña:
      <br>
      <input type="password" id="password" v-model="registro.password">
    </label>
    <br>
    <label>
      Conocimientos
    </label>
    <br>
    <label for="HTML">HTML <input type="checkbox" id="HTML" v-model="registro.opciones" value="HTML"></label>
    <label for="CSS">CSS <input type="checkbox" id="CSS" v-model="registro.opciones" value="CSS"></label>
    <label for="javascript">javascript <input type="checkbox" id="javascript" v-model="registro.opciones" value="javascript"></label>
    <br>
    <label for="administrador"></label>
    <input type="checkbox" v-model="registro.administrador">
    ¿Usuario administrador?
    <br>
    <label for="observaciones"><strong>Comentario:</strong></label>
    <br>
    <textarea name="observaciones" id="observaciones" cols="30" rows="5" v-model="registro.observaciones"></textarea>
    <br>
    <label for="grupo">
      grupo
      <select name="grupo" id="grupo" v-model="registro.grupo">
        <option value="0" selected>...</option>
        <optgroup label="seccion 1">
          <option value="1-1">1</option>
          <option value="1-2">2</option>
          <option value="1-3">3</option>
          <option value="1-4">4</option>
        </optgroup>
        <optgroup label="seccion 2">
          <option value="2-1">1</option>
          <option value="2-2">2</option>
          <option value="2-3">3</option>
          <option value="2-4">4</option>
        </optgroup>
      </select>
    </label>
    <br>
    <button @click="guardar" class="btnGuardar">Guardar</button>
    <button @click="restablecer" class="btnRestablecer">Restablecer</button>
    <br>
    <div class="divYa">
    <a href="" class="yaCuenta">Ya tengo cuenta</a>
  </div>

    </form> 
  </WelcomeItem>
</template>


