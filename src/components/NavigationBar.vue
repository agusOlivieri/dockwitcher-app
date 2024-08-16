<script setup>
import { defineProps } from 'vue'

defineProps({
  title: {
    type: String,
    default: () => ''
  },
  subtitle: {
    type: String,
    default: () => ''
  }
})
</script>

<template>
  <nav class="navigation-bar d-flex align-items-start">
    <ul class="w-100 px-4 mt-2 d-flex justify-content-between">
      <li class="d-flex align-items-center">
        <span class="me-4 fs-5 fw-medium">{{ subtitle }}</span>
        <font-awesome-icon icon="fa-solid fa-house" />
        <span class="ms-1 fs-5 fw-medium">{{ title }}</span><span class="enabled ms-1 fs-5 fw-medium">- {{ subtitle }}</span>
      </li>
      <li>
        <button class="btn btn-navigation-bar">Importar</button>
      </li>
    </ul>
  </nav>
</template>
