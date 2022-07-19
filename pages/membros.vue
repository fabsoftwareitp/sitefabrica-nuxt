<script setup>
const { path } = useRoute()
const navigationTree = await fetchContentNavigation(queryContent(path))
const links = navigationTree[0].children

</script>
<template>
  <main>
    <div v-for="item in links" class="flex justify-center flex-wrap">
      <div class="flex flex-col items-center justify-center">
        <img :src="item.img" alt="Imagem {{ item.name }}" class="w-[150px] rounded-full">
        <h3 class="text-center text-black text-2xl font-semibold">{{ item.name }}</h3>
      </div>
    </div>
  </main>
</template>
