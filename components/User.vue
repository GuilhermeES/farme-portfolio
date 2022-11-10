<template>
    <div class="user">
        <img src="~/assets/img/farme_index.png" alt="Guilherme" />
        <h1 class="title">
            Guilherme Souza dos Santos
        </h1>
    </div>
</template>

<style lang="scss">
    .user{
        display: flex;
        align-items: center;
        padding-top: 50px;
        gap: 40px;
        width: 70%;
    }
    @media(max-width:996px) {
        .user{
            width: 100%;
        }
    }
</style>