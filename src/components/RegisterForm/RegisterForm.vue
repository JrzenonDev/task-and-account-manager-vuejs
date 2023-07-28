<template>
  <form>
    <v-text-field
      v-model="state.name"
      :error-messages="v$.name.$errors.map((e) => e.$message)"
      :counter="10"
      label="Seu nome completo"
      required
      @input="v$.name.$touch"
      @blur="v$.name.$touch"
    ></v-text-field>

    <v-text-field
      v-model="state.email"
      :error-messages="v$.email.$errors.map((e) => e.$message)"
      label="E-mail"
      required
      @input="v$.email.$touch"
      @blur="v$.email.$touch"
    ></v-text-field>

    <v-text-field
      v-model="state.password"
      :error-messages="v$.password.$errors.map((e) => e.$message)"
      :counter="10"
      label="Senha"
      required
      @input="v$.password.$touch"
      @blur="v$.password.$touch"
    ></v-text-field>

    <v-text-field
      v-model="state.confirmPassword"
      :error-messages="v$.confirmPassword.$errors.map((e) => e.$message)"
      :counter="10"
      label="Repita a senha"
      required
      @input="v$.confirmPassword.$touch"
      @blur="v$.confirmPassword.$touch"
    ></v-text-field>

    <v-btn class="me-4" @click="v$.$validate"> Enviar </v-btn>
  </form>
</template>
<script setup>
import { reactive } from 'vue'
import { useVuelidate } from '@vuelidate/core'
import { email, required } from '@vuelidate/validators'

const initialState = {
  name: '',
  email: '',
  password: '',
  confirmPassword: ''
}

const state = reactive({
  ...initialState
})

const rules = {
  name: { required },
  email: { required, email },
  password: { required },
  confirmPassword: { required }
}

const v$ = useVuelidate(rules, state)
</script>
