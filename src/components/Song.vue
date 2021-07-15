<template>
    <div class="song-container"> 
        <div class="box">
            <img :src="poster">
            <span class="title">{{title}}</span>
            <p class="author">{{author}}</p>
            <p class="year">{{year}}</p>
            </div>
    </div>
</template>

<script>
export default {
    name: "Song",
    props: {
        poster: String,
        title: String,
        author: String,
        year: String,
    }
}
</script>


<style lang="scss" scoped>

    .song-container{
        text-align: center;

        .box{
            background-color: #2E3A46;
            padding: 15px;
            height: 350px;
            margin-bottom: 20px;
        }

        .title{
            color:white;
            font-weight: bold;
            font-size: 20px;
        }

        .author{
            font-size:20px;
            color: grey;
        }

        .year{
            font-size: 18px;
            color: grey;
        }

        .genre{
            color:grey;
            font-size: 18px;

        }

        img{
            width:100%;
            padding-bottom: 10px
        };
    }

</style>