<script setup>
const items = ref([
  {
    label: 'เกี่ยวกับเรา',
    to: '/base/about',
    icon: 'lucide:table-columns-split'
  }, {
    label: 'ข้อมูลครู',
    to: '/base/teacher',
    icon: 'lucide:user-round-check'
  }, {
    label: 'ข้อมูลนักเรียน',
    to: '/base/student',
    icon: 'lucide:user-round-check'
  }
])
</script>


<template>
  <UHeader title="Web-IT">
    <template #left>
      <h1 class="me-10 text-red-950 hover:text-red-600 text-2xl font-bold">
        <NuxtLink to="/">Web-IT</NuxtLink>
      </h1>
      <div class="hidden md:flex">
        <ul class="flex gap-8">
          <li v-for="item in items" :key="item.to" class="cursor-pointer hover:text-red-700">
            <NuxtLink :to="item.to">
              <UIcon :name="item.icon"></UIcon> {{ item.label }}
            </NuxtLink>
          </li>
        </ul>
      </div>
    </template>
    <template #body>
      <UNavigationMenu :items="items" orientation="vertical" mode="slideover" class="-mx-2.5 flex w-1/2 content-end" />
    </template>
    <template #right>
      <NuxtLink to="/login">
        <UIcon name="lucide:door-closed-locked"></UIcon> สมาชิก
      </NuxtLink>
    </template>

  </UHeader>
  <UContainer class="mt-10">
    <slot />
  </UContainer>
</template>