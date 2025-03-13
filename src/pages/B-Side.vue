<!-- Start Generation Here -->
<template>
  <Navbar />
<v-container>
  <v-row>
    <v-col>
      <h1>B-Side</h1>
      <p>Bienvenido a la sección B-Side de mi blog.</p>
      <v-btn color="primary" @click="goBack">Regresar</v-btn>
    </v-col>
  </v-row>
</v-container>
</template>

<script setup>
import Navbar from '@/components/Navbar.vue';
import { useRouter } from 'vue-router';

const router = useRouter();

function goBack() {
router.push('/');
}
</script>

<style scoped>
h1 {
color: #1976d2;
}
</style>
<!-- End Generation Here -->
