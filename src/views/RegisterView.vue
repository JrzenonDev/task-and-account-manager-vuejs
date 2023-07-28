<script setup>
import RegisterForm from '../components/RegisterForm/RegisterForm.vue'
</script>

<template>
  <v-container>
    <v-row>
      <v-col row="6">
        <h1 class="title tagline">
          <span class="accent">Seja</span> muito<br />Bem <span class="accent">vindo!</span>
        </h1>
        <p>
          Esta aplicação permitirá que você controle o seu fluxo de tarefas diárias.<br />
          Além disso, também permitirá que você controle o seu fluxo de gastos.
        </p>
        <p class="text-regiter">
          Realize o seu cadastro e comece agora a organizar suas rotinas, obtendo um melhor controle
          do seu dia a dia.
        </p>
        <p class="text-login">Já é cadastrado? <a class="link-login" href="#">Clique aqui!</a></p>
      </v-col>
      <v-col row="6">
        <RegisterForm />
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
.tagline {
  background: -webkit-linear-gradient(315deg, #42d392 25%, #647eff);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.accent {
  background: -webkit-linear-gradient(315deg, #42d392 25%, #647eff);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
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
