<template>
    <div id ='app'>
        <Header />
        <Main :Songs="Songs" />
    </div>
</template>

<script>
//IMPORTAZIONE COMPONENTI NELL'APP.VUE
import axios from 'axios';
import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  //ESPORTAZIONE IN ALTRE COMPONENTI (RENDIAMO QUESTE COMPONENTI ACCESSIBILI AD ALTRE COMPONENTI)
    name: 'App',
    components:{
      Header,
      Main
    },

    data() {
      return{
        Songs: []
      }
    },
    created(){    //quando abbiamo richiamato tutte le API necessarie allora Songs verrà popolato
      axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
      this.Songs = result.data.response
    })
    }
}
</script>

