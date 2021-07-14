<template>

<section>
    <div class="container">
        <div class="row">
            <div class="d-flex flex-wrap justify-content-center">
                <Song class="central col-2 mx-3"
                v-for= "(Song, index) in Songs" 
                :key= "index"  
                :poster= "Song.poster" 
                :title= "Song.title" 
                :author= "Song.author"
                :year= "Song.year" 
                />
            </div>
        </div>
    </div>
</section>

</template>

<script>
import Song from "../components/Song.vue"
export default {
    name:'Main',
    components: {
        Song     //Componente Aggiunto
    },
    props: {
        Songs: Array, //Regitriamo l'attributo Songs(Array di oggetti pescati dall'API) in Main.vue cosi da poterci lavorare sopra
    }

}
</script>

<style lang="scss" scoped>
</style>