<script setup lang="ts">

import { useRoute } from 'vue-router'
import { onMounted, watch } from 'vue'

const route = useRoute()

onMounted(() => console.log('Fetching data inside onMounted'))

watch(() => route.params.id, () => console.log('Fetching inside watch'), { immediate: true })

</script>

<template>
  <div>Recipe View {{ route.params.id }}</div>
  <nav>
    <ul>
      <li>
        <RouterLink :to="{name: 'recipe', params: {id: 1}}">Recipe 1</RouterLink>
      </li>
      <li>
        <RouterLink :to="{name: 'recipe', params: {id: 3}}">Recipe 3</RouterLink>
      </li>
    </ul>
  </nav>
</template>

<style scoped>

</style>