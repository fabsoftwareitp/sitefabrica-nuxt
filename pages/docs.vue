<script setup>
const { path } = useRoute()
const navigationTree = await fetchContentNavigation(queryContent(path))
const links = navigationTree[0].children

</script>
<template>
  <main>
    <header class="bg-black mb-10">
      <Navbar />
    </header>
    <h1 class="text-center text-[#FD624C] font-bold text-3xl underline decoration-wavy mb-6">
      Documentos
    </h1>
    <div class="flex justify-center flex-wrap max-w-[1000px] m-auto">
      <div v-for="(item, index) in links">
        <NuxtLink :to="item._path">
          {{item.name}}
        </NuxtLink>
      </div>
    </div>
  </main>
</template>
