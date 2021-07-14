<template>
<div class="nav-bar">
    <div class="logo">
        <img src="../assets/spotify-logo.png">
    </div>
</div>
</template>

<script>

export default {
    name: 'Header',
}
</script>


<style lang="scss" scoped>
    .nav-bar{
        background-color: #2E3A46;
        margin-bottom: 40px;

        .logo{
            height: 80px;
            width: 80px;
            display: flex;
            align-items: center;
            margin-left: 20px;

            img{
                width: 100%;
            }
        }
    }
</style>