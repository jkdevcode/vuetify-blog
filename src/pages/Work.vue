<template>
  <div class="container-work">
  <div>
      <Navbar />
      <h2 class="text-h2 text-center text--white work">View Work</h2>
      <v-img class="mb-4" height="150" src="@/assets/logo.png" />
    </div>
  </div>
</template>

<script setup>
import Navbar from "@/components/Navbar.vue";
</script>

<style scoped>
.container-work {
  height: 100vh;
  display: flex;
  flex-direction: column; /* Organiza los elementos en columna */
  background-color: #f8f6fe;


}

.work {
  font-size: 2rem;
  font-weight: bold;
}
</style>
