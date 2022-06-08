<template>
  <section>
        <div class="container pt-5">
            <div class="row">
                <AlbumCard class="col-12 col-sm-5 col-md-3 col-lg-2"  v-for="(album, index) in albums" :key="index" :album="album"/>    
            </div>
        </div>
        <div class="container">
            <div class="row">

            </div>
        </div>
  </section>
</template>

<script>
 
import axios from 'axios';
    import AlbumCard from '../commons/AlbumCard';
    export default {
        name: 'SectionAlbums',
        components: {
            AlbumCard,
        },
        data() {
            return {
                albums: [],
            };
        },
        created() {
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((response) => {
                this.albums = response.data.response;
            })
        }
    }
</script>

<style lang="scss" scoped>

</style>