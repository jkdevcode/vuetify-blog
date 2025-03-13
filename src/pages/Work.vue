<template>
  <div>
    <Navbar />
    <h2 class="text-h2 text-center mt-10 work">View Work</h2>
    <v-img
        class="mb-4"
        height="150"
        src="@/assets/logo.png"
      />
  </div>
</template>

<script setup>
import Navbar from '@/components/Navbar.vue';

</script>

<style scoped>
.work {
  font-size: 2rem;
  font-weight: bold;
  color: black;
}
</style>
