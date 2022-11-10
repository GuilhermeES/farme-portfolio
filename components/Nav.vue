<template>
    <div>
        <nav class="navigation">
            <ul class="navigation__items" v-if="size">
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
            <div class="social-media" v-if="size">
                <a href="https://www.behance.net/guilhermesouzasantos" target="_blank" class="behance">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M7.443 5.35c.639 0 1.23.05 1.77.198a3.83 3.83 0 0 1 1.377.544c.394.247.689.594.885 1.039.197.445.295.99.295 1.583 0 .693-.147 1.286-.491 1.731-.295.446-.787.841-1.377 1.138.836.248 1.475.693 1.868 1.286.394.594.64 1.336.64 2.177 0 .693-.148 1.286-.394 1.781-.246.495-.639.94-1.082 1.237a5.078 5.078 0 0 1-1.573.692c-.59.149-1.18.248-1.77.248H1V5.35h6.443zm-.394 5.54c.541 0 .984-.148 1.328-.395.344-.247.492-.693.492-1.237 0-.297-.05-.594-.148-.791-.098-.198-.246-.347-.442-.495-.197-.099-.394-.198-.64-.247-.246-.05-.491-.05-.787-.05H4v3.216h3.05zm.148 5.838c.295 0 .59-.05.836-.099a1.72 1.72 0 0 0 .688-.297 1.76 1.76 0 0 0 .492-.544c.098-.247.197-.544.197-.89 0-.693-.197-1.188-.59-1.534-.394-.297-.935-.445-1.574-.445H4v3.81h3.197zm9.492-.05c.393.396.983.594 1.77.594.541 0 1.033-.148 1.426-.395.394-.297.64-.594.738-.891h2.41c-.394 1.187-.984 2.028-1.77 2.572-.788.495-1.722.792-2.853.792a5.753 5.753 0 0 1-2.115-.396 3.93 3.93 0 0 1-1.574-1.088 3.93 3.93 0 0 1-.983-1.633c-.246-.643-.345-1.335-.345-2.127 0-.742.099-1.434.345-2.078a5.34 5.34 0 0 1 1.032-1.682c.443-.445.984-.84 1.574-1.088a5.49 5.49 0 0 1 2.066-.396c.836 0 1.574.149 2.213.495.64.346 1.131.742 1.525 1.336a6.01 6.01 0 0 1 .885 1.88c.098.692.147 1.385.098 2.176H16c0 .792.295 1.534.689 1.93zm3.098-5.194c-.344-.346-.885-.544-1.525-.544-.442 0-.787.099-1.082.247-.295.149-.491.347-.688.545a1.322 1.322 0 0 0-.344.692c-.05.248-.099.445-.099.643h4.426c-.098-.742-.344-1.236-.688-1.583zM15.459 6.29h5.508v1.336H15.46V6.29z"/></svg>
                </a>
                <a href="https://www.linkedin.com/in/guilherme-souza-designer/" target="_blank" class="linkedin">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="24" height="24"><path fill="none" d="M0 0h24v24H0z"/><path d="M6.94 5a2 2 0 1 1-4-.002 2 2 0 0 1 4 .002zM7 8.48H3V21h4V8.48zm6.32 0H9.34V21h3.94v-6.57c0-3.66 4.77-4 4.77 0V21H22v-7.93c0-6.17-7.06-5.94-8.72-2.91l.04-1.68z"/></svg>
                </a>
            </div>
        </nav>
        <div class="mobile" v-if="!size">
            <div class="mobile__page btn">
                {{routeName}}
            </div>
            <div class="btn-mobile" @click="menuClick">
                <div class="btn-mobile__line"></div>
                <div class="btn-mobile__line"></div>
                <div class="btn-mobile__line"></div>
            </div>
            <div class="mobile__layer" v-show="menuOpen"></div>
            <div class="mobile__menu" v-show="menuOpen">
                <div class="mobile__top">
                    <div class="mobile__close">
                        <svg @click="menuClick" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="40" height="40"><path fill="none" d="M0 0h24v24H0z"/><path d="M12 10.586l4.95-4.95 1.414 1.414-4.95 4.95 4.95 4.95-1.414 1.414-4.95-4.95-4.95 4.95-1.414-1.414 4.95-4.95-4.95-4.95L7.05 5.636z" fill="rgba(255,255,255,1)"/></svg>
                    </div>
                </div>
                <div class="mobile__farme">
                    <img src="~/assets/img/farme_mobile.png" alt="Guilherme" />
                </div>
                <nav>
                    <li class="mobile__navigation"> 
                        <NuxtLink to="/" class="mobile__link">Início</NuxtLink>
                    </li>
                    <li class="mobile__navigation"> 
                        <NuxtLink to="/sobre" class="mobile__link">Sobre</NuxtLink>
                    </li>
                    <li class="mobile__navigation"> 
                        <NuxtLink to="/projetos" class="mobile__link">Projetos</NuxtLink>
                    </li>
                </nav>
                <div class="mobile__social-media">
                    <a href="https://www.behance.net/guilhermesouzasantos" target="_blank" class="behance">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="30" height="30"><path fill="none" d="M0 0h24v24H0z"/><path d="M7.443 5.35c.639 0 1.23.05 1.77.198a3.83 3.83 0 0 1 1.377.544c.394.247.689.594.885 1.039.197.445.295.99.295 1.583 0 .693-.147 1.286-.491 1.731-.295.446-.787.841-1.377 1.138.836.248 1.475.693 1.868 1.286.394.594.64 1.336.64 2.177 0 .693-.148 1.286-.394 1.781-.246.495-.639.94-1.082 1.237a5.078 5.078 0 0 1-1.573.692c-.59.149-1.18.248-1.77.248H1V5.35h6.443zm-.394 5.54c.541 0 .984-.148 1.328-.395.344-.247.492-.693.492-1.237 0-.297-.05-.594-.148-.791-.098-.198-.246-.347-.442-.495-.197-.099-.394-.198-.64-.247-.246-.05-.491-.05-.787-.05H4v3.216h3.05zm.148 5.838c.295 0 .59-.05.836-.099a1.72 1.72 0 0 0 .688-.297 1.76 1.76 0 0 0 .492-.544c.098-.247.197-.544.197-.89 0-.693-.197-1.188-.59-1.534-.394-.297-.935-.445-1.574-.445H4v3.81h3.197zm9.492-.05c.393.396.983.594 1.77.594.541 0 1.033-.148 1.426-.395.394-.297.64-.594.738-.891h2.41c-.394 1.187-.984 2.028-1.77 2.572-.788.495-1.722.792-2.853.792a5.753 5.753 0 0 1-2.115-.396 3.93 3.93 0 0 1-1.574-1.088 3.93 3.93 0 0 1-.983-1.633c-.246-.643-.345-1.335-.345-2.127 0-.742.099-1.434.345-2.078a5.34 5.34 0 0 1 1.032-1.682c.443-.445.984-.84 1.574-1.088a5.49 5.49 0 0 1 2.066-.396c.836 0 1.574.149 2.213.495.64.346 1.131.742 1.525 1.336a6.01 6.01 0 0 1 .885 1.88c.098.692.147 1.385.098 2.176H16c0 .792.295 1.534.689 1.93zm3.098-5.194c-.344-.346-.885-.544-1.525-.544-.442 0-.787.099-1.082.247-.295.149-.491.347-.688.545a1.322 1.322 0 0 0-.344.692c-.05.248-.099.445-.099.643h4.426c-.098-.742-.344-1.236-.688-1.583zM15.459 6.29h5.508v1.336H15.46V6.29z"/></svg>
                    </a>
                    <a href="https://www.linkedin.com/in/guilherme-souza-designer/" target="_blank" class="linkedin">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" width="30" height="30"><path fill="none" d="M0 0h24v24H0z"/><path d="M6.94 5a2 2 0 1 1-4-.002 2 2 0 0 1 4 .002zM7 8.48H3V21h4V8.48zm6.32 0H9.34V21h3.94v-6.57c0-3.66 4.77-4 4.77 0V21H22v-7.93c0-6.17-7.06-5.94-8.72-2.91l.04-1.68z"/></svg>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                windowWidth: 996,
                menuOpen: false
            }
        },
        mounted () {
            this.windowWidth = window.innerWidth
        },
        computed: {
            size(){
                if(this.windowWidth > 996){
                    return true
                }
                else{
                    return false
                }
            },
            routeName(){
                if(this.$route.path == '/'){
                    return 'Início'
                }
                else if(this.$route.path == '/sobre'){
                    return 'Sobre'
                }
                else{
                    return 'Projetos'
                }
            },
        }, 
        methods : {
            menuClick() {
                this.menuOpen = !this.menuOpen
            }
        }    
    }
</script>

<style scoped lang="scss">
    .navigation{
        display: flex;
        align-items: center;
        justify-content: space-between;

        &__items{
            display: flex;
            gap: 20px;
            padding-left: 0;
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

        .social-media{
            .behance{
                margin-right: 10px;
            }
            svg{
                transition: .5s;
                &:hover{
                    fill: var(--secondary);
                }
            }
        }
    }
    /*Menu mobile*/
    .mobile{
        display: flex;
        align-items: center;
        justify-content: space-between;

        &__page{
            background-color: var(--main);
            height: 26px;
        }

        .btn-mobile{
            background: #FFFFFF;
            border: 2px solid #000000;
            box-shadow: 2px 2px 0px #000000;
            border-radius: 4px;
            padding: 10px;
            width: 32px;
            float: right;
            cursor: pointer;

            &__line{
                width: 32px;
                height: 3px;
                background-color: #000000;
                margin-bottom: 10px;
                &:nth-child(3){
                    margin-bottom: 0;
                }
            }

            &:active{
                background-color: var(--secondary);
            }
        }

        &__layer{
            position: absolute;
            width: 100%;
            z-index: 99;
            background: rgb(0 0 0 / 70%);
            left: 0;
            bottom: 0;
            top: 0;
        }

        &__menu{
            background: #FFFFFF;
            border: 1.48305px solid #000000;
            box-shadow: 2.9661px 2.9661px 0px #000000;
            border-radius: 5.9322px;
            height: 550px;
            position: absolute;
            left: 30px;
            right: 30px;
            top: 100px;
            z-index: 100;
        }

        
        &__top{
            background-color: var(--secondary);
            width: 100%;
            height: 120px;
            border-top-left-radius: 5px;
            border-top-right-radius: 5px;
        }

        &__close{
            float: right;
            padding: 20px;
        }

        &__farme{
            text-align: center;
            position: relative;
            bottom: 30px;
        }

        &__navigation{
            text-align: center;
            margin-bottom: 30px;
        }

        &__link{
            font-family: var(--font);
            text-decoration: none;
            font-size: 25px;
            color: #000000;
            font-weight: 700;
        }

        &__social-media{
            position: absolute;
            bottom: 0;
            width: 100%;
            border-top: 1px solid;
            height: 100px;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 30px;
        }
    }
</style>