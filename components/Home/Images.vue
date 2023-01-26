<script setup>
const images = [
  { rotationClass: 'rotate-2', src: 'https://images.unsplash.com/photo-1672426193314-0c06224b2e50?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1374&q=80' },
  { rotationClass: '-rotate-2', src: 'https://images.unsplash.com/photo-1672594522674-b2f295a9932e?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1374&q=80' },
  { rotationClass: 'rotate-2', src: 'https://images.unsplash.com/photo-1673006768363-e09be1444330?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1665&q=80' },
  { rotationClass: '-rotate-2', src: 'https://images.unsplash.com/photo-1593062096033-9a26b09da705?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=3270&q=80' },
  { rotationClass: 'rotate-2', src: 'https://images.unsplash.com/photo-1508193638397-1c4234db14d8?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1374&q=80' },
]
</script>

<template>
  <div class="mt-16 sm:mt-20">
    <div class="flex justify-center gap-5 py-4 -my-4 sm:gap-8">
      <div v-for="(image, index) in images" :key="index" :class="image.rotationClass"
        class="relative aspect-[9/10] w-44 flex-none overflow-hidden rounded-xl bg-zinc-800 sm:w-60 sm:rounded-2xl">
        <img alt="" :src="image.src" class="absolute inset-0 object-cover w-full h-full">
      </div>
    </div>
  </div>
</template>
