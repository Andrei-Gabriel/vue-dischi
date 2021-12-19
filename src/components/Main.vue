<template>
    <section class="list-container">
        <SearchBar @ricerca="metodoRicerca"/>
        <div v-if="albums != null" class="contain">
            <div class="card" v-for="(album, index) in albumsFiltered" :key="index">
                <Card :info="album"/>
            </div>  
        </div>
        <div v-else class="loader">
            Loading
        </div>
    </section>
</template>

<script>
import axios from 'axios';
import Card from './subsections/Card.vue';
import SearchBar from './subsections/SearchBar.vue';

export default {
    name: 'Main',
    components: {
        Card,
        SearchBar,
    }, 
    data() {
        return {
            albums: null,
            albumsFiltered: null,
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((albums) => {
            this.albums = albums.data.response;
            this.albumsFiltered = albums.data.response;
        })
    },
    methods: {
        metodoRicerca(research) {
            this.albumsFiltered = this.albums.filter((elem) => {
                return elem.title.toLowerCase().includes(research.toLowerCase());
            });
        }
  }
}
</script>

<style lang="scss" scoped>
    .list-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        .contain {
        width: 1200px;
        margin: 30px auto;
        display: flex;
        flex-wrap: wrap;
        // Proprietà card
        .card {
        padding: 20px;
        min-height: 370px;
        max-height: 370px;
        overflow-y: scroll;
        width: calc(20% - 40px);
        margin: 10px 20px;
        background-color: #2e3a46;
        }
        }
        .loader {
            color: white;
            font-size: 50px;
        }
    }
</style>