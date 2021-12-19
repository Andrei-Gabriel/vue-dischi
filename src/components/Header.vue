<template>
    <header>
        <i class="fab fa-spotify"></i>
        <!-- <img src="../assets/logo-small.svg" alt=""> -->
        <form class="search">
            <input class="text-search" type="text" placeholder="Cerca" v-model="testoRicerca">
            <button class="btn-search" @click.prevent="$emit('ricerca', testoRicerca)">cerca</button>
        </form>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            testoRicerca: "",
        }
    }
}
</script>

<style lang="scss" scoped>    
    header {
        height: 70px;
        background-color: #2e3a46;
        padding: 0 30px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        // img {
        //     height: 50px;
        //     filter: invert(20%) sepia(52%) saturate(4154%) hue-rotate(73deg) brightness(88%) contrast(90%);
        // }
        // Logo
        i {
            font-size: 55px;
            color: #1ed760;
            background-color: #000;
            border-radius: 50%;
        }
        .text-search, .btn-search{
            border: none;
            line-height: 1.8;
            border-radius: 7px;
            padding: 0 7px;
        }
        .text-search {
            background-color: #e9e9ed;
        }
        .btn-search {
            text-transform: uppercase;
            margin-left: 5px;
        }
    }
</style>