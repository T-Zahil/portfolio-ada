<script setup>
import { experiences } from '~/config'
</script>

<template>
  <div class="relative px-4 sm:px-8 lg:px-12">
    <div class="max-w-2xl mx-auto lg:max-w-5xl">
      <header class="max-w-2xl">
        <h1 class="text-4xl font-bold tracking-tight text-zinc-100 sm:text-5xl">
          I had A LOT of experiences. Everyone wants to hire me.
        </h1>
        <p class="mt-6 text-base text-zinc-400">
          And here is the list of all my experiences. Maybe the next one will be with you?
        </p>
      </header>
      <div class="mt-16 sm:mt-20">
        <div class="md:border-l md:pl-6 md:border-zinc-700/40">
          <div class="flex flex-col max-w-3xl space-y-16">
            <article v-for="experience in experiences" :key="experience.date"
              class="md:grid md:grid-cols-4 md:items-baseline">
              <div class="relative flex flex-col items-start md:col-span-3 group">
                <h2 class="text-base font-semibold tracking-tight text-zinc-100">
                  <div
                    class="absolute z-0 transition scale-95 opacity-0 -inset-y-6 -inset-x-4 group-hover:scale-100 group-hover:opacity-100 bg-zinc-800/50 sm:-inset-x-6 sm:rounded-2xl">
                  </div>
                  <a :href="experience.url">
                    <span class="absolute z-20 -inset-y-6 -inset-x-4 sm:-inset-x-6 sm:rounded-2xl">
                    </span>
                    <span class="relative z-10">{{ `${experience.position} at ${experience.company}` }}</span>
                  </a>
                </h2>
                <time class="md:hidden relative z-10 order-first mb-3 flex items-center text-sm text-zinc-500 pl-3.5"
                  datetime="2022-09-05">
                  <span class="absolute inset-y-0 left-0 flex items-center" aria-hidden="true">
                    <span class="h-4 w-0.5 rounded-full bg-zinc-500">
                    </span>
                  </span>{{ experience.date }}</time>
                <p class="relative z-10 mt-2 text-sm text-zinc-400">
                  {{ experience.description }}
                </p>
              </div>
              <time class="relative z-10 flex items-center order-first mt-1 mb-3 text-sm md:block text-zinc-500"
                datetime="2022-09-05">{{ experience.date }}</time>
            </article>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
