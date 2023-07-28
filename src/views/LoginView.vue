<script setup>
import LoginForm from '../components/LoginForm/LoginForm.vue'
</script>

<template>
  <v-container>
    <v-row>
      <v-col row="6">
        <h1 class="title tagline"><span class="accent">Vamos</span> começar?</h1>
        <p>Faça o seu login e comece a sua organização de tarefas e contas.</p>
        <p class="text-regiter">
          Receba notificações de tarefas com prazo perto de expirar, saiba quais contas estão
          próximo do vencimento
        </p>
        <p class="text-login">
          Não é cadastrado?
          <router-link class="link-login" to="/register">Clique aqui!</router-link>
        </p>
      </v-col>
      <v-col row="6">
        <LoginForm />
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.title {
  font-size: 76px;
  line-height: 1.25;
  font-weight: 900;
}

.text-regiter {
  color: #42d392;
  font-style: italic;
  font-weight: bold;
  font-size: 18px;
}

.text-login {
  font-size: 15px;
  margin-top: 15px;
  text-transform: uppercase;
}
.link-login {
  font-weight: bold;
  border: 1px solid;
  border-radius: 5px;
  padding: 3px 14px;
  transition: 0.5s;
}

.link-login:hover {
  background-color: hsla(160, 100%, 37%, 0.2);
}
</style>
