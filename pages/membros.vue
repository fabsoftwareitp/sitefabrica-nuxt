<script setup>
const { path } = useRoute()
const navigationTree = await fetchContentNavigation(queryContent(path))
const links = navigationTree[0].children

</script>
<template>
  <main>
    <head>
      <Title>Membros</Title>
    </head>
    <header class="bg-black mb-10">
      <Navbar />
    </header>
    <h1 class="text-center text-[#FD624C] font-bold text-3xl underline decoration-wavy mb-6">
      Todos os Membros
    </h1>
    <div class="flex justify-center flex-wrap max-w-[1000px] m-auto">
      <div v-for="item in links">
        <NuxtLink :to="item.way">
          <div v-if="item.img" class="flex text-center text-black text-2xl font-semibold items-center flex-col justify-center m-[10px] w-[270px] h-[200px] border shadow-xl shadow-black rounded-lg hover:bg-black hover:text-[#FD624C] hover:shadow-white duration-200 hover:underline">
            <img :src="item.img" :alt="item.name" class="w-[150px] rounded-full">
            <h3>
              {{ item.name }}
            </h3>
          </div>
        </NuxtLink>
      </div>
    </div>
  </main>
</template>
