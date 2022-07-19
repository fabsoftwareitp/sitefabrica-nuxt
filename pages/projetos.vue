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
    <h1 class="text-center text-[#FD624C] font-bold text-3xl underline decoration-wavy">Todos os Projetos</h1>
    <div class="flex justify-center flex-wrap max-w-[1000px] m-auto">
      <div v-for="item in links">
        <div class="flex items-center flex-col justify-center m-[25px] w-[450px] h-[250px]">
          <img :src="item.img" :alt="item.name" class="h-[200px]">
          <NuxtLink :to="item.way">
            <h3 class="text-center text-black text-2xl font-semibold">
              {{ item.name }}
            </h3>
          </NuxtLink>
        </div>
      </div>
    </div>
  </main>
</template>
