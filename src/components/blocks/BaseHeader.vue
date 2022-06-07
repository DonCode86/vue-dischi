<template>
  <header>
      <div class="header-container">
        <img src="..\src\img\spotify-logo.png" alt=""> 
      </div>
  </header>
</template>

<script>
export default {
    name: 'BaseHeader'
}
</script>

<style lang="scss" scoped>

header {
    background-color: var(--secondary-color);
    img {
    height: 2.5rem;
    width: 3.6875rem;
    margin: .625rem .9375rem;
    }

}
</style>