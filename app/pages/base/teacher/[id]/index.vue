<script setup>
const route = useRoute()
const id = route.params.id
</script>

<template>
  <div>
    <h1>Teacher with ID = {{ id }}</h1>
  </div>
</template>