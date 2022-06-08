<template>
    <main>
    <SelectBar/>
    <SectionAlbums/>
    </main>
</template>

<script>
import SelectBar from '../commons/SelectBar.vue';
import SectionAlbums from '../sections/SectionAlbums.vue';

export default {
    name: 'BaseMain',
    components: {
        SelectBar,
        SectionAlbums 
    },
}

</script>

<style lang="scss" scoped>
main {
    background-color: var(--primary-color);
    height: calc(100vh - 3.75rem);
}
</style>