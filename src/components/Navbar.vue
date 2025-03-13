<template>

    <div>
    <!-- Barra de navegación -->
    <v-app-bar flat color="#f8f6fe">
      <v-toolbar-title class="mr-auto">Mi Blog</v-toolbar-title>

      <!-- Ícono de menú hamburguesa en móviles -->
      <v-app-bar-nav-icon
        v-if="$vuetify.display.smAndDown"
        @click.stop="drawer = !drawer"
      ></v-app-bar-nav-icon>

      <!-- Botones de navegación visibles en pantallas grandes -->
      <template v-if="$vuetify.display.mdAndUp">
        <v-btn text to="/">Inicio</v-btn>
        <v-btn text to="/b-side">B-Side</v-btn>
      </template>
    </v-app-bar>

    <!-- Menú lateral en dispositivos móviles -->
    <v-navigation-drawer
      v-model="drawer"
      :location="$vuetify.display.mobile ? 'bottom' : 'right'"
      temporary
      color="#F5F5F5"
    >
      <v-list>
        <v-list-item to="/" @click="drawer = false">
          <v-list-item-title class="text">Inicio</v-list-item-title>
        </v-list-item>
        <v-list-item to="/b-side" @click="drawer = false">
          <v-list-item-title class="text">B-Side</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    </div>
<!-- #F8F6FE -->
</template>

<script setup>
import { ref } from "vue";

const drawer = ref(false);
</script>

<style scoped>
.text {
  color: black;
  font-size: 1.2rem;
}
</style>
