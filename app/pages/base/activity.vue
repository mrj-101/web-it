<script setup>
const acts = await $fetch("http://www.rvc.ac.th:9000/api/activity?status=1&limit=6")
console.log(acts);
</script>

<template>
  <div>
    <h1 class="text-2xl text-blue-600 mb-8">กิจกรรมภายในวิทยาลัย</h1>
    
    <UPageGrid>
      <div v-for="act in acts.data" :key="act.activity_id">
        <img :src="act.thumbnail" alt="pic">
        <h2>{{ act.activity }}</h2>
        <p>{{ act.dt }}</p>
      </div>
    </UPageGrid>

  </div>
</template>