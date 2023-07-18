<script lang="ts" setup>
import { menu } from '~/config'
</script>

<template>
  <div class="z-10 flex justify-center pt-6">
    <nav>
      <ul class="flex px-3 text-sm font-medium border rounded-full shadow-lg bg-zinc-800 text-zinc-200 border-zinc-700">
        <li v-for="link in menu" :key="link.name">
          <NuxtLink :to="link.path" class="relative block px-3 py-2 transition dark:hover:text-primary-400">
            {{ link.name }}
          </NuxtLink>
        </li>
      </ul>
    </nav>
  </div>
</template>
