<template>
  <div class="album-card m-3 p-2">
      <img class="album-img" :src="album.poster" :alt="album.title">
        <h5 class="album-title text-white mt-3">{{album.title}}</h5>
        <span class="album-author">{{album.author}}</span>
        <small class="album-year">{{album.year}}</small>
  </div>
</template>

<script>
export default {
    name: 'AlbumCard.vue',
   props: {
      album: Object,
   }

}
</script>

<style lang="scss" scoped>
.album-card{
   background-color: var(--secondary-color);
   text-align: center;
   img{
      width: 100%;
      margin-top: 0.625rem;
   }
   .album-year, .album-author{
         color: gray;
      }
     
}

</style>