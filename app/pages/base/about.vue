<template>
  <div class="grid grid-cols-1 md:grid-cols-4 gap-8 gap-y-4 justify-between">
    <div v-for="i in 5" :key="i" class="border p-3 rounded-2xl shadow-2xl">
      <h3 v-if="i % 2 == 0" class="text-2xl font-extrabold text-red-700">Title {{ i }}</h3>
      <h3 v-else class="text-2xl font-extrabold">Title {{ i }}</h3>
      Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ea eius iste ipsa assumenda
      accusamus inventore
      voluptatum modi officiis voluptatibus rerum libero earum facilis eveniet, vel quisquam aut, voluptatem aliquam
      possimus.
    </div>
  </div>
</template>