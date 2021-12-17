<template>
    <section class="list-container">
        <div class="card" v-for="(album, index) in albums" :key="index">
            <Card :info="album"/>
        </div>
    </section>
</template>

<script>
import axios from 'axios';
import Card from './subsections/Card.vue';

export default {
    name: 'Main',
    components: {
        Card,
    }, 
    data() {
        return {
            albums: null
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((albums) => {
            this.albums = albums.data.response;
        })
    },
}
</script>

<style lang="scss" scoped>
    .list-container {
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
</style>