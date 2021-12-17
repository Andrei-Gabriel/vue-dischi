<template>
    <div class="album">
        <img :src="info.poster">
        <h3>{{info.title}}</h3>
        <span class="name">{{info.author}}</span>
        <span class="date">{{info.year}}</span>
    </div>
</template>

<script>
export default {
    name: 'Card',
    props: {
        info: Object
    }
}
</script>

<style lang="scss" scoped>
    .album {
        display: flex;
        flex-direction: column;
        align-items: center;
        img {
            width: 100%;
        }
        h3 {
            margin: 15px 0 10px;
            font-size: 24px;
            text-transform: uppercase;
            color: #fdfefd;
            text-align: center;
        }
        .name {
            color: #726f66;
            font-size: 20px;
        }
        .date {
            color: #726f66;
            font-size: 18px;
        }
    }
</style>