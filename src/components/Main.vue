<template>
    <section class="list-container">
        <Card/>
    </section>
</template>

<script>
import Card from './subsections/Card.vue';
export default {
    name: 'Main',
    components: {
        Card,
    }
}
</script>

<style lang="scss" scoped>
    .list-container {
        width: 1200px;
        margin: 30px auto;
        display: flex;
        flex-wrap: wrap;
    }
</style>