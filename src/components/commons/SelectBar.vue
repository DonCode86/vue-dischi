<template>
   <section>
        <div class="select">
            <select name="type" id="type" v-model="select.value">
                <option value="All">Tutti i generi</option>
                <option value="Rock">Rock</option>
                <option value="Pop">Pop</option>
                <option value="Jazz">Jazz</option>
                <option value="Metal">Metal</option>
            </select>
        </div>
    </section>
</template>

<script>
import select from '../../shared/selected.js';

export default {
    name: 'SelectBar',
    data() {
        return {
            select
        };
    },
}
</script>

<style lang="scss" scoped>
select {
  appearance: none;
  outline: 0;
  border: 0;
  box-shadow: none;
  flex: 1;
  padding: 0 1em;
  color: #fff;
  background-color: var(--darkgray);
  background-image: none;
  cursor: pointer;
}

select::-ms-expand {
  display: none;
}

.select {
  position: relative;
  display: flex;
  width: 20em;
  height: 3em;
  border-radius: .25em;
  overflow: hidden;
  margin: auto;
}

.select::after {
  content: '\25BC';
  position: absolute;
  top: 0;
  right: 0;
  padding: 1em;
  background-color: #34495e;
  transition: .25s all ease;
  pointer-events: none;
}

.select:hover::after {
  color: greenyellow;
}


</style>