<template>
  <v-app-bar app>
    <v-toolbar-title class="mr-auto">Mi Blog</v-toolbar-title>

    <!-- Menú hamburguesa visible solo en pantallas pequeñas -->
    <v-app-bar-nav-icon @click="drawer = !drawer" v-if="display.smAndDown"></v-app-bar-nav-icon>

    <!-- Drawer para el menú -->
    <v-navigation-drawer v-model="drawer" app>
      <v-list>
        <v-list-item to="/">
          <v-list-item-title>Inicio</v-list-item-title>
        </v-list-item>
        <v-list-item to="/b-side">
          <v-list-item-title>B-Side</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <!-- Botones de navegación visibles solo en pantallas grandes -->
    <v-btn text to="/" v-if="display.mdAndUp">Inicio</v-btn>
    <v-btn text to="/b-side" v-if="display.mdAndUp">B-Side</v-btn>
  </v-app-bar>
</template>

<script setup>
import { ref } from 'vue';
import { useDisplay } from 'vuetify';

const drawer = ref(false);

// Utilizamos useDisplay para obtener el objeto de visualización y los puntos de ruptura
const display = useDisplay();
</script>

<style scoped></style>
