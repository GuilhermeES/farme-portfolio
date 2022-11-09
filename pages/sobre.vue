<template>
  <div>
    <div class="content">
    <Nav />
    <div class="user">
      <img src="~/assets/img/farme_sobre.png" alt="Guilherme" />
      <h1 class="title">
        Um pouco <br> sobre mim
      </h1>
    </div>
    <p class="text">
      Sou UI/UX designer, atualmente graduando em Publicidade e
      propaganda. Trabalhei na área do design gráfico de 2019 a 2021.
      Comecei com a criação peças para impressão utilizando as ferramentas da Adobe,
      a partir disso, comecei a desenvolver artes voltadas a social media para diversos
      clientes com diferentes propostas, sempre focando na qualidade e
      seguindo o manual de marca de cada cliente. Atualmente, trabalho
      e busco me especializar na área de UX/UI design.<br><br>

      Já trabalhei com diversas tecnologias, como, Photoshop, Illustrator, After effects, Premiere e Figma.
    </p>
    <NuxtLink to="/projetos" class="btn btn--main">Confira meus projetos</NuxtLink>
  </div>
  <Copy />
  </div>
</template>


<style scoped lang="scss">
  .text {
    width: 65%;
    padding-bottom: 20px;
  }

  @media(max-width:996px) {
    .text {
      width: 100%;
    }
  }

</style>
