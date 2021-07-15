  
<template>
    <div id ='app'>
      <!-- Se l'array Songs non viene popolato allora faremo un display del Loader -->
       <Loader v-if="Songs.length == 0" />
        <Header :Songs="Songs" />
        <Main :Songs="filteredSongs" /> //
    </div>
</template>

<script>
//IMPORTAZIONE COMPONENTI NELL'APP.VUE
import axios from 'axios';
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Loader from './components/Loader.vue';



export default {
  //ESPORTAZIONE IN ALTRE COMPONENTI (RENDIAMO QUESTE COMPONENTI ACCESSIBILI AD ALTRE COMPONENTI)
    name: 'App',
    components:{
      Header,
      Main,
      Loader,
    },
    data() {
      return{
        Songs: [], //Data/input dove l'utente inserirà la voce 
        inputSong: ''
       }
  },


    created(){    //quando abbiamo richiamato tutte le API necessarie allora Songs verrà popolato
      axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
      this.Songs = result.data.response
    })
    },
  methods: {

  }
}

</script>

<style lang="scss">
@import "./style/app.scss";
</style>