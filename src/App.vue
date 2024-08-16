<script setup>
import { RouterView, useRoute } from 'vue-router'
import { ref, watch } from 'vue'

import HeaderBar from './components/HeaderBar.vue'
import Sidebar from '@/components/Sidebar.vue'
import NavigationBar from './components/NavigationBar.vue'

const route = useRoute()

const pageTitle = ref('')
const pageSubtitle = ref('')

// Función para actualizar el título y subtítulo
const updateTitles = () => {
  // Establecer el título desde la ruta padre (route.matched[0])
  pageTitle.value = route.matched[0]?.meta.title || ''
  // Establecer el subtítulo desde la ruta actual (route.meta)
  pageSubtitle.value = route.meta.subtitle || ''
}

// Inicializar los valores al montar el componente
updateTitles()

//Observar los cambios en la ruta
watch(route, () => {
  updateTitles()
})
</script>

<template>
  <Sidebar />
  <div class="w-100">
    <div class="headers w-100">
      <HeaderBar />
      <div class="line"></div>
      <NavigationBar :subtitle="pageSubtitle" :title="pageTitle"/>
    </div>
    <div class="mx-4 workarea">
      <RouterView />
    </div>
  </div>
</template>
