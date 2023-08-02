<script setup>
import { ref} from 'vue'

const registro = ref({
  email: '',
  password: '',
})

const guardar = (e) => {
  e.preventDefault();
  console.log(registro.value);
  cambio.value=false
}

const restablecer = (e) => {
  e.preventDefault();
  //Limpiar los campos
  email.value = '';
  password.value = '';
  
}

let cambio = ref(true)

</script>

<template>
  <div class="about">
    <form >
      <h2>Log in</h2>
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
    <br><br>
    <button @click="guardar" class="btnGuardar">Guardar</button>
    <button @click="restablecer" class="btnRestablecer">Restablecer</button>
    </form>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}

.btnGuardar{
  margin-right: 10px;
  
}
</style>
