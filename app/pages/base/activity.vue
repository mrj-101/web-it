<script setup>
const { error, pending, data } = useFetch('http://www.rvc.ac.th:9000/api/activity?status=1')
console.log(data.value)
</script>

<template>
  <div>
    <h1>Activity</h1>

  </div>
</template>