<script setup>
const data = await $fetch("http://www.rvc.ac.th:9000/api/activity?status=1")
// const { error, pending, data } = await useFetch('http://www.rvc.ac.th:9000/api/activity?status=1')
</script>

<template>
  <div>
    <h1 class="text-2xl text-blue-600 mb-8">กิจกรรมภายในวิทยาลัย</h1>
    {{ data }}
  </div>
</template>