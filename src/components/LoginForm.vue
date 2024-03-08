<script setup lang="ts">
import InputText from 'primevue/inputtext';
import Password from 'primevue/password';
import Button from 'primevue/button';
import {ref} from 'vue'

const username = ref('')
const password = ref('')

</script>

<template>
  <div>Zaloguj się</div>
  <form>
    <div class="input-container">
      <label for="username">Nazwa użytkownika</label>
      <InputText id="username" type="text" v-model="username"/>
    </div>
    <div class="input-container">
      <label for="password">Hasło</label>
      <Password id="password" v-model="password" :feedback="false"/>
    </div>
    <Button label="Submit"/>
  </form>
  <p>{{ username }}</p>
</template>

<style scoped>
.input-container {
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding-top: 10px;
}
</style>