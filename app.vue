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


h1 {
  color: #FD624C;
  text-align: center;
  font-size: 2.8em;
  font-weight: 600;
  margin-top: 10px;
}

img {
  margin: auto;
  width: 300px;
  border-radius: 50%;
  padding: 20px;
}

h2 {
  color: #FD624C;
  text-align: center;
  font-size: 1.8em;
  font-weight: 600;
}

h4 {
  color: #FD624C;
  text-align: center;
  font-size: 1.4em;
  font-weight: 600;
}

p {
  font-size: 1.2em;
  width: 1200px;
  margin: auto;  
}

li {
  width: 450px;
  margin: auto;
  font-size: 1.2em;
}
</style>
