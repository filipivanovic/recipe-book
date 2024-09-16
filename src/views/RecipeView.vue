<script setup lang="ts">

import { useRoute } from 'vue-router'

const route = useRoute()

</script>

<template>
  <div>Recipe View {{ route.params.id }}</div>
</template>

<style scoped>

</style>