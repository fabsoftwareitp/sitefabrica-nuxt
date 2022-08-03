<template>
  <div class="">
    <Html lang="pt-br" />
    <Meta property="og:image" content="/cover.jpg" />
    <Meta name="twitter:card" content="summary_large_image" />
    <div class="text-white">
      <NuxtPage />
      <footer class="bg-black pt-6 pb-6">
        <h3 class="text-center text-[#FD624C] font-bold">Copyright © 2020 - 2022 Fábrica de softwares ITP - IFSP - Todos os direitos reservados</h3>
      </footer>
    </div>
  </div>
</template>

<style lang="postcss">

#imagem-fundo {
  height: 100vh;
  background: linear-gradient(rgba(0, 0, 0, 0.65), rgba(0, 0, 0, 0.7)), url('https://images.pexels.com/photos/270360/pexels-photo-270360.jpeg?auto=compress cs=tinysrgb&w=1260&h=750&dpr=1');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
