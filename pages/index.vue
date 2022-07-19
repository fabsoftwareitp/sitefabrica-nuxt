<script setup>
const navigationMembros = await fetchContentNavigation(queryContent('/membros'))
const navigationProjetos = await fetchContentNavigation(queryContent('/projetos'))
const membros = navigationMembros[0].children
const projetos = navigationProjetos[0].children
</script>

<template>
  <div>
    <div id="imagem-fundo">
      <Navbar />
      <div class="mt-12 mx-auto h-5/6">
        <div class="relative">
          <img src="../public/logo-oficial.png" alt="Logo Fábrica de Software" class=" d-block mx-auto w-56 drop-shadow-2xl hover:animate-bounce">
        </div>
        <div>
          <h1 class="mt-12 text-center text-6xl sm:text-7xl font-semibold text-slate-200 tracking-tight">
            Fábrica de Software
          </h1>
          <h2 class="font-bold text-transparent text-4xl bg-clip-text bg-gradient-to-r from-orange-400 to-[#FD624C] text-center">
            IFSP Itapetininga
          </h2>
        </div>
      </div>
    </div>
    <div class="text-2xl flex justify-around mt-20">
      <article class="text-left text-black w-96">
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vero facilis velit minima delectus harum praesentium maiores et a, molestias placeat earum magni perspiciatis itaque? Deserunt tempore consectetur necessitatibus eum ratione.</p>

        <img src="../public/icone-tecnologia.png" alt="Icone Tecnologia" class="w-1/2 m-auto mt-4">

        <h2 class="text-[#FD624C] text-center text-3xl font-semibold pt-10 underline decoration-wavy">Tecnologias</h2>
      </article>
      <article class="text-center text-black w-96">
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vero facilis velit minima delectus harum praesentium maiores et a, molestias placeat earum magni perspiciatis itaque? Deserunt tempore consectetur necessitatibus eum ratione.</p>

        <img src="../public/desafio.png" alt="desafio" class="w-1/2 m-auto mt-10">

        <h2 class="text-[#FD624C] text-center text-3xl font-semibold pt-4 underline decoration-wavy">Desafios</h2>
      </article>
      <article class="text-right text-black w-96">
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Vero facilis velit minima delectus harum praesentium maiores et a, molestias placeat earum magni perspiciatis itaque? Deserunt tempore consectetur necessitatibus eum ratione.</p>

        <img src="../public/equipe.png" alt="Equipe" class="w-1/2 m-auto mt-6">

        <h2 class="text-[#FD624C] text-center text-3xl font-semibold pt-8 underline decoration-wavy">Equipes</h2>
      </article>
    </div>
    <div>
      <h2 class="text-center text-black font-bold text-3xl mt-28 mb-10">
        Membros Ativos
      </h2>
      <div class="flex justify-center flex-wrap max-w-[1000px] m-auto">
        <div v-for="membro in membros">
          <div v-if="membro.status === 'ativo'" class="flex items-center flex-col justify-center m-[10px] w-[270px] h-[200px]">
            <img :src="membro.img" alt="Imagem {{ item.name }}" class="w-[150px] rounded-full">
            <NuxtLink :to="membro.way">
              <h3 class="text-center text-black text-2xl font-semibold">
                {{ membro.name }}
              </h3>
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
    <div>
      <h2 class="text-center text-black font-bold text-3xl mt-6 mb-10">
        Projetos Em Andamento
      </h2>
      <div class="flex justify-center flex-wrap max-w-[1000px] m-auto">
        <div v-for="projeto in projetos">
          <div v-if="projeto.status === 'ativo'" class="flex items-center flex-col justify-center m-[25px] w-[450px] h-[250px]">
            <img :src="projeto.img" :alt="projeto.name" class="h-[200px]">
            <NuxtLink :to="projeto.way">
              <h3 class="text-center text-black text-2xl font-semibold">
                {{ projeto.name }}
              </h3>
            </NuxtLink>
          </div>
        </div>
      </div>
    </div>
    <div>
      <h2 class="text-center text-black font-bold text-3xl mt-6">
        Depoimentos
      </h2>
      <section class="flex justify-around mt-10 flex-wrap w-full">
        <div class="mb-10 shadow-2xl bg-[#0200B3] rounded-xl">
          <iframe class="w-[40vw] h-[40vh]" src="https://www.youtube.com/embed/B1bys3rAuL8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;encrypted-media; gyroscope; picture-in-picture" allowfullscreen />
          <h3 class="text-center text-[#FD624C] font-bold text-2xl p-1.5">
            Rafael Damiam
          </h3>
        </div>
        <div class="mb-10 shadow-2xl bg-[#0200B3] rounded-xl">
          <iframe class="w-[40vw] h-[40vh]" src="https://www.youtube.com/embed/sDcW1keRIDs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;encrypted-media; gyroscope; picture-in-picture" allowfullscreen />
          <h3 class="text-center text-[#FD624C] font-bold text-2xl p-1.5">
            Vinicius Zevarex
          </h3>
        </div>
        <div class="mb-10 shadow-2xl bg-[#0200B3] rounded-xl">
          <iframe class="w-[40vw] h-[40vh]" src="https://www.youtube.com/embed/D054k8JNOm4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;encrypted-media; gyroscope; picture-in-picture" allowfullscreen />
          <h3 class="text-center text-[#FD624C] font-bold text-2xl p-1.5">
            João Morais
          </h3>
        </div>
        <div class="mb-10 shadow-2xl bg-[#0200B3] rounded-xl">
          <iframe class="w-[40vw] h-[40vh]" src="https://www.youtube.com/embed/aw3LTiobEYs" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write;encrypted-media; gyroscope; picture-in-picture" allowfullscreen />
          <h3 class="text-center text-[#FD624C] font-bold text-2xl p-1.5">
            Lucas Cavalherie
          </h3>
        </div>
      </section>
    </div>
  </div>
</template>
