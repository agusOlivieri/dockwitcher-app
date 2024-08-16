<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <div class="sidebar">
    <div class="title-container">
      <h2 class="title">dockwitcher</h2>
    </div>
    <div class="line"></div>
    <div class="side-options mt-4">
      <ul class="px-2">
        <li>
          <div class="d-flex justify-content-between align-items-center">
            <div class="d-flex container-option">
              <div class="d-flex align-items-center justify-content-center">
                <font-awesome-icon icon="fa-solid fa-sliders" />                
              </div>
              <span class="fw-medium">Camiones</span>
          </div>
            <button
              class="btn btn-primary p-0"
              id="collapse-btn"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#collapseCamiones"
              aria-expanded="false"
              aria-controls="collapseCamiones"
            >
              <font-awesome-icon icon="fa-solid fa-angle-down" id="collapse-icon" />
            </button>
          </div>
          <div class="collapse" id="collapseCamiones">
            <div class="container-option d-flex">
              <div></div>
              <div class="w-auto">
                <p class="my-1"><RouterLink to="/trucks">Camiones</RouterLink></p>
                <p class="my-1"><RouterLink to="/drivers">Conductores</RouterLink></p>
              </div>
            </div>
          </div>
        </li>
        <li>
          <div class="d-flex justify-content-between align-items-center">
            <div class="d-flex container-option">
              <div class="d-flex align-items-center justify-content-center">
                <font-awesome-icon icon="fa-solid fa-sliders" />                
              </div>
              <span class="fw-medium">Planificación</span>
            </div>
            <button
              class="btn btn-primary p-0"
              id="collapse-btn"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#collapsePlanificacion"
              aria-expanded="false"
              aria-controls="collapsePlanificacion"
            >
              <font-awesome-icon icon="fa-solid fa-angle-down" id="collapse-icon" />
            </button>
          </div>
          <div class="collapse" id="collapsePlanificacion">
            <div class="container-option d-flex">
              <div></div>
              <div class="w-auto">
                <p class="my-1"><RouterLink to="/planning/dashboard">Panel</RouterLink></p>
                <p class="my-1"><RouterLink to="/planning/incommings">Recepciones</RouterLink></p>
                <p class="my-1"><RouterLink to="/planning/outgoings">Expediciones</RouterLink></p>
              </div>
            </div>
          </div>
        </li>
        <li>
          <div class="d-flex container-option">
            <div class="d-flex align-items-center justify-content-center">
              <font-awesome-icon icon="fa-solid fa-truck-ramp-box" />              
            </div>
            <span class="fw-medium">Control de muelle</span>
          </div>
        </li>
        <li>
          <div class="d-flex container-option">
            <div class="d-flex align-items-center justify-content-center">
              <font-awesome-icon icon="fa-solid fa-truck-moving" />
            </div>
            <span class="fw-medium">Transporte</span>
          </div>
        </li>
        <li>
          <div class="d-flex container-option">
            <div class="d-flex align-items-center justify-content-center">
              <font-awesome-icon icon="fa-solid fa-gear"/>
            </div>
            <span class="fw-medium">Configuración</span>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
