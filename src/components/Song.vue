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
        year: String
    }
}
</script>