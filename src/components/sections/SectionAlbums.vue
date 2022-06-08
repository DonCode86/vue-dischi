<template>
         <div class="container pt-5">
            <div class="row">
                <AlbumCard class="col-12 col-sm-5 col-md-3 col-lg-2"  v-for="(album, index) in filterAlbum " :key="index " :album="album"/>    
            </div>
        </div>
  
</template>

<script>
 
import axios from 'axios';
    import AlbumCard from '../commons/AlbumCard';
    import selected from '../../shared/selected';
    export default {
        name: 'SectionAlbums',
        components: {
            AlbumCard,
        },
        data() {
            return {
                albums: [],
                selected
            };
        },
        created() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((response) => {
                this.albums = response.data.response;
            })
        },
        computed:{
        filterAlbum(){
        return this.albums.filter((elm) => elm.genre === this.selected.value || this.selected.value === 'All');
      }
    },
}
</script>

<style lang="scss" scoped>


</style>