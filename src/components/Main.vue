<template>

<section>
    <div class="container type">
        <div class="row typeo">
            <div>
                <Song class="central col-2 .justify-content-center"
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