<script setup>
const { path } = useRoute()
const navigationTree = await fetchContentNavigation(queryContent(path))
const links = navigationTree[0].children

</script>
<template>
  <main>
    <h1>alow</h1>

    <ul id="example-1">
      <li v-for="link in links" :key="link._path">
        <NuxtLink :to="link._path">
          {{ link.title }}
        </NuxtLink>
      </li>
    </ul>
  </main>
</template>
