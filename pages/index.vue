<template>
  <div>
    <div class="content">
      <Nav />
      <div class="user">
        <img src="~/assets/img/farme_index.png" alt="Guilherme" />
        <h1 class="title">
          Guilherme Souza dos Santos
        </h1>
      </div>
      <div class="inside">
        <div class="inside__tag btn">
          UX/UI Designer
        </div>
        <p class="text">
          Olá, sou um designer <strong>apaixonado por tecnologia.</strong> Adoro criar interfaces que sejam ao mesmo
          tempo bonitas e funcionais.
        </p>
        <NuxtLink to="/projetos" class="btn btn--main">Confira meus projetos</NuxtLink>
      </div>
    </div>
    <Copy />
  </div>
</template>

<script>
  export default {
    name: 'IndexPage',
  }

</script>

<style scoped lang="scss">
  .inside {
    &__tag {
      background-color: var(--secondary);
      width: 166px;
      color: #ffffff;
      height: 26px;
      text-align: center;
    }

    .text {
      padding-top: 20px;
      padding-bottom: 20px;
      width: 54%;
    }
  }

  @media(max-width:996px) {
    .inside {
      &__tag{
        margin-top: 32px;
      }
      .text {
        width: 100%;
      }
    }
  }

</style>
