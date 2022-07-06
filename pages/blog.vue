<script setup>
const { path } = useRoute()
const navigationTree = await fetchContentNavigation(queryContent(path))
const links = navigationTree[0].children

</script>
<template>
  <Navbar />
  <h1>Posts</h1>

  <ul id="example-1">
    <li v-for="link in links" :key="link._path">
      <NuxtLink :to="link._path">
        {{ link.title }}
      </NuxtLink>
    </li>
  </ul>
</template>
