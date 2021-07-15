<template>
<div class="nav-bar">
        <div class="logo">
            <img src="../assets/spotify-logo.png">
        </div>
        <div class="menu-list">
         <label class="mx-3" for = 'mySelect'>Select a song</label>
            <select id="mySelect">
                <option>TEST</option>
                <option>TEST</option>
                <option>TEST</option>
                <option>TEST</option>
                <option>TEST</option>
                <option>TEST</option>
            </select>
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
        display:flex;
        align-items:center;
        justify-content: space-between;

        .logo{
            height: 100%;
            width: 80px;
            margin-left: 20px;


            img{
                width: 100%;
            }
        }
        .menu-list{
            margin-right: 40px;   
            color: burlywood;
            font-weight: bold;
        }
    }
</style>