<template>
  <div class="flex flex-col h-full bg-black">
    <Navbar />
    <div class="fixed inset-0 flex justify-center overflow-x-hidden sm:px-8 customScrollbar">
      <div class="flex justify-center w-full max-w-7xl lg:px-8">
        <div class="flex justify-center w-full h-fit">
          <div
            class="flex flex-col justify-between w-full h-full pt-24 mx-4 my-12 ring-2 bg-zinc-900 ring-zinc-300/20 rounded-xl customSize">
            <NuxtPage />
            <Footer />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
html {
  @apply bg-black;
}

.customSize {
  max-width: calc(100vw - 2rem);
}

/* width */
.customScrollbar::-webkit-scrollbar {
  width: 10px;
  display: none;
  scrollbar-gutter: stable both-edges;
}

.customScrollbarVisible::-webkit-scrollbar {
  width: 10px;
  display: block;
  scrollbar-gutter: stable both-edges;
}

.customScrollbar:hover::-webkit-scrollbar {
  display: block;
  scrollbar-gutter: stable both-edges;
}

/* Track */
.customScrollbar::-webkit-scrollbar-track,
.customScrollbarVisible::-webkit-scrollbar-track {
  @apply bg-zinc-800 rounded-lg;
}

/* Handle */
.customScrollbar::-webkit-scrollbar-thumb,
.customScrollbarVisible::-webkit-scrollbar-thumb {
  @apply bg-zinc-700 rounded-lg;
}

/* Handle on hover */
.customScrollbar::-webkit-scrollbar-thumb:hover,
.customScrollbarVisible::-webkit-scrollbar-thumb:hover {
  @apply bg-zinc-600;
}
</style>
