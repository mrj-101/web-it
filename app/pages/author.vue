<script setup>
    // let name = ref("นายสุระชัย วิเศษโวหาร")
    // let age = ref(17)
    let names = ref([
        { name: "ทักษิณ", age: 18 },
        { name: "ยิ่งรัก", age: 18 },
        { name: "แพร", age: 18 },
    ])
</script>

<template>
    <div>
        <h1>ผู้จัดทำ</h1>

        <UTable :data="names" class="flex-1" />
    </div>
</template>

<style scoped>
    h1 {
        color: red;
    }
</style>