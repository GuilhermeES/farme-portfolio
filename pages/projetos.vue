<template>
  <div>
    <div class="content">
      <Nav />
      <div class="user">
        <img src="~/assets/img/farme_projetos.png" alt="Guilherme" />
        <h1 class="title">
          Meus projetos
          de design
        </h1>
      </div>
      <div class="projects">
        <div class="projects__item">
          <a href="https://www.behance.net/gallery/156922421/App-ajudeme" target="_blank">
            <img src="~/assets/img/ajudeme.png" alt="ajude.me" />
            <div class="projects__info">
              <div class="projects__name">
                ajude.me
              </div>
              <img src="~/assets/img/Figma.png" alt="Figma" class="projects__tols" />
            </div>
          </a>
        </div>
        <div class="projects__item">
          <a href="https://www.behance.net/gallery/147955887/Redesign-Orkut" target="_blank">
            <img src="~/assets/img/redesign_orkut.png" alt="Redesign Orkut" />
            <div class="projects__info">
              <div class="projects__name">
                Redesign Orkut
              </div>
              <img src="~/assets/img/Figma.png" alt="Figma" class="projects__tols" />
            </div>
          </a>
        </div>
        <div class="projects__item">
          <a href="https://www.behance.net/gallery/144397809/Strong-fitness-app" target="_blank">
            <img src="~/assets/img/strongapp.png" alt="Strong app" />
            <div class="projects__info">
              <div class="projects__name">
                Strong app
              </div>
              <img src="~/assets/img/Figma.png" alt="Figma" class="projects__tols" />
            </div>
          </a>
        </div>
        <div class="projects__item">
          <a href="https://www.behance.net/gallery/156489541/Redesign-Site-Pat-Lab" target="_blank">
            <img src="~/assets/img/petlab.png" alt="Site-Pat Lab" />
            <div class="projects__info">
              <div class="projects__name">
                Site-Pat Lab
              </div>
              <img src="~/assets/img/Figma.png" alt="Figma" class="projects__tols" />
            </div>
          </a>
        </div>
        <div class="projects__item">
          <a href="https://www.behance.net/gallery/145169441/Healthtech-Landing-page" target="_blank">
            <img src="~/assets/img/landing.png" alt="Landing page" />
            <div class="projects__info">
              <div class="projects__name">
                Landing page
              </div>
              <img src="~/assets/img/Figma.png" alt="Figma" class="projects__tols" />
            </div>
          </a>
        </div>
        <div class="projects__item">
          <a href="https://www.behance.net/gallery/144397809/Strong-fitness-app" target="_blank">
            <img src="~/assets/img/motion.png" alt="Motion Graphics" />
            <div class="projects__info">
              <div class="projects__name">
                Motion Graphics
              </div>
              <img src="~/assets/img/Figma.png" alt="Figma" class="projects__tols" />
              <img src="~/assets/img/after.png" alt="Figma" class="projects__tols" />
            </div>
          </a>
        </div>
      </div>
    </div>
    <Copy />
  </div>
</template>


<style scoped lang="scss">
  .projects{
    display: flex;
    flex-wrap: wrap;
    gap: 40px;
    width: 100%;
    padding-top: 32px;

    &__item{
      background: #FFFFFF;
      width: 172px;
      border: 2px solid #000000;
      box-shadow: 3px 3px 0px #000000;
      border-radius: 9px;
      transition: .2s;
      a{
        text-decoration: none;
      }
      img{
        border-top-left-radius: 9px;
        border-top-right-radius: 9px;
      }
      &:hover{
        box-shadow: 6px 6px 0px #000000;
      }
    }

    &__info{
      padding: 10px;
    }

    &__name{
      color: #000000;
      font-family: var(--font-secondary);
      font-weight: 700;
    }

    &__tols{
      padding-top: 20px;
    }
  }
  @media(max-width:996px){
    .projects{
      width: 100%;
      gap: 20px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      justify-content: center;
    }
  }
</style>
