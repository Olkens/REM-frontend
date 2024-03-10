<script setup lang="ts">
import InputText from 'primevue/inputtext';
import Password from 'primevue/password';
import Button from 'primevue/button';
import {reactive} from 'vue'
import axios from "axios";


const loginData = reactive({
  email: '',
  password: ''
})

const handleLogin = () => {
  console.log('login')
  axios.post('http://localhost:6969/login', loginData).then(res => {
    console.log(res)
  }).catch(e => {
    console.log(e)
  })
}

</script>

<template>
  <div>Zaloguj się</div>
  <form @submit.prevent="handleLogin" >
    <div class="input-container">
      <label for="username">Nazwa użytkownika</label>
      <InputText id="username" type="text" v-model="loginData.email"/>
    </div>
    <div class="input-container">
      <label for="password">Hasło</label>
      <Password id="password" v-model="loginData.password" :feedback="false"/>
    </div>
    <Button label="Submit" type="submit"/>
  </form>
</template>

<style scoped>
.input-container {
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding-top: 10px;
}
</style>