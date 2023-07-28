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
          <a href="https://github.com/JrzenonDev/" target="_blank"
            >JrzenonDev <img class="github-icon" src="../../assets/images/github.svg"
          /></a>
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
.content-footer {
  position: absolute;
  bottom: 0;
  right: 0;
  left: 0;
  text-align: center;
}
.github-icon {
  color: hsla(160, 100%, 37%, 1);
}
</style>
