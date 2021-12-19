<template>
    <header>
        <i class="fab fa-spotify"></i>
        <!-- <img src="../assets/logo-small.svg" alt=""> -->
    </header>
</template>

<script>
export default {
    name: 'Header',
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
    }
</style>