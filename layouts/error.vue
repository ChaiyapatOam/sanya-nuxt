<template>
  <div class="container p-5">
    <h1 v-if="error.statusCode === 404">404 Page not found</h1>
    <h1 v-else>ขออภัยเกิดข้อผิดพลาด</h1>
    <NuxtLink to="/">กลับหน้าหลัก</NuxtLink>
  </div>
</template>

<script>
export default {
  props: ['error'],
}
</script>
