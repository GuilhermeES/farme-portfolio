<template>
    <div class="copy">
        <div class="copy__inside">
            <div class="copy__item">
                <div class="copy__dev">
                    Desenvolvido por:
                </div>
                <div class="copy__person">
                    <a href="https://main--guilherme-es-portfolio.netlify.app/" target="_blank">
                        Guilherme Estevão Silva
                    </a>
                </div>
            </div>
            <div class="copy__item">
                <div class="copy__dev">
                    Designer por:
                </div>
                <div class="copy__person">
                    <NuxtLink to="/">
                        Guilherme Souza dos Santos
                    </NuxtLink>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped lang="scss">
    .copy{
        background: #E7E7E7;
        width: 100%;
        padding-top: 40px;
        padding-bottom: 40px;


        &__inside{
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            gap: 40px;
        }


        &__dev{
            color: var(--text);
            font-family: var(--font);
            font-weight:700 ;
            opacity: .5;
        }

        &__person{
           a{
            color: var(--text);
            font-family: var(--font);
            font-weight: 500 ;
            opacity: .5;
            text-decoration: none;
           }
        }
    }

    @media(max-width:996px) {
        .copy{
            &__inside{
                width: 100%;
                max-width: 100%;
                padding-left: 15px;
                padding-right: 15px;
            }
        }
    }
    @media(max-width:556px) {
        .copy{
            &__inside{
                display: block;
                text-align: center;
            }
        }
    }
</style>