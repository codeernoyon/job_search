<template>
  <div class="bg-teal-800 min-h-screen min-w-full">
    <Nav />
    <NuxtPage />
    <Footer />
  </div>
</template>
<script setup>
const active = usePopUpActive().value;
</script>
