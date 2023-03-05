<script setup>
import { ref } from 'vue'
const valor = ref(0)

function login() {
  if (usuario.value == 'prueba' && contraseña.value == '1234') {
    alert(attribs.value.valor)
  } else {
    alert('datos incorrectos')
  }
}

const attribs = ref({
  valor: 1,
})
</script>

<template>
  <header>Reseña de peliculas</header>

  <section>
    <div>
      <h2>Felicidades iniciaste sesion!</h2>
    </div>
    <div>
      <h2>Inicia sesion</h2>

      <label for="usuario">Usuario: </label>
      <input type="text" id="usuario" v-model="usuario" placeholder="Nombre de usuario" />
      <br />

      <label for="contraseña">Contraseña: </label>
      <input type="text" id="contraseña" v-model="contraseña" placeholder="contraseña" />
      <br />
    </div>
  </section>
  <button @click="login()">Iniciar Sesion</button>
</template>

<style>
header {
  font-size: 20px;
  text-align: center;
  font-weight: bold;
  padding: 10px;
  background-color: #e4e881;
}
h2 {
  text-align: center;
  color: Blue;
}
input {
  margin: 10px;
  margin-left: 10px;
}
label {
  margin: 1.5em;
}
section {
  margin: 10px;
  width: 100%;

  border: 1px solid black;
  border-radius: 15px;
}
button {
  text-align: center;
  margin: 10px;
  border-radius: 15px;
  font-size: 10px;
  padding: 10px;
  background-color: cyan;
}
</style>
