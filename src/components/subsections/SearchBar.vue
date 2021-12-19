<template>
    <div>
        <form class="search">
            <input class="text-search" type="text" placeholder="Cerca" v-model="testoRicerca">
            <button class="btn-search" @click.prevent="$emit('ricerca', testoRicerca)">cerca</button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'SearchBar',
    data() {
        return {
            testoRicerca: "",
        }
    }
}
</script>

<style lang="scss" scoped>
    div {
        margin-top: 30px;
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