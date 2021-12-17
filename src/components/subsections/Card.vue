<template>
    <div class="card">
        <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg">
        <h3>New Jersey</h3>
        <span class="name">Bon Jovi</span>
        <span class="date">1988</span>
    </div>
</template>

<script>
export default {
    name: 'Card',
}
</script>

<style lang="scss" scoped>
    .card {
        padding: 20px;
        display: flex;
        flex-direction: column;
        align-items: center;
        min-height: 350px;
        max-height: 350px;
        overflow-y: scroll;
        width: calc(20% - 40px);
        margin: 10px 20px;
        background-color: #2e3a46;
        img {
            width: 100%;
        }
        h3 {
            margin: 15px 0 10px;
            font-size: 26px;
            text-transform: uppercase;
            color: #fdfefd;
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