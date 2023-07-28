<script setup lang="ts">
import { ref } from 'vue'

const getCurrentYear = () => new Date().getFullYear()
const currentYear = ref(getCurrentYear())
</script>

<template>
  <v-container class="content-footer">
    <v-row>
      <v-col cols="12">
        <p>Released under the MIT License.</p>
        <p>
          Copyright © {{ currentYear }}
          <a href="https://github.com/JrzenonDev/" target="_blank">JrzenonDev</a>
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.content-footer {
  text-align: center;
}
</style>
