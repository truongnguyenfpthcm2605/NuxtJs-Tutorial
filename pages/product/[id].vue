<template>
  <h1>Đây La Product id : {{ $route.params.id }}</h1>
</template>

<script setup>
  const nuxt = useNuxtApp();
  console.log(nuxt)
</script>
