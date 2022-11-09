<template>
    <nav class="navigation">
        <ul class="navigation__items">
            <li class="navigation__item"> 
                <NuxtLink to="/" class="navigation__link btn">Início</NuxtLink>
            </li>
            <li class="navigation__item">
                <NuxtLink to="/sobre" class="navigation__link btn">Sobre</NuxtLink>
            </li>
            <li class="navigation__item">
                <NuxtLink to="/projetos" class="navigation__link btn">Projetos</NuxtLink>
            </li>
        </ul>
    </nav>
</template>

<style scoped lang="scss">
    .navigation{
        width: 50%;

        &__items{
            display: flex;
            gap: 20px;
            padding-left: 0;
        }

        &__item{
            list-style: none;
        }

        &__link{
            color: #000000;
            background-color: transparent;
            &.nuxt-link-exact-active{
                background-color: var(--main);
            }
            &:hover{
                background-color: var(--secondary);
                color: #ffffff;
                transition: .5s;
            }
        }
    }
</style>