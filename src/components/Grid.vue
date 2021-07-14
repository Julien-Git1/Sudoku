<template>
  <div class="grid">
    <span v-for="cell in table" :key="cell.id">
      <span v-for="cell1 in cell.ligne" :key="cell1.id"> {{cell1}}</span>
    </span>

  </div>
</template>

<script>
export default {
  name: "Grid",
  props: {
    msg: String,
    table: Array,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.grid span{
    display: Grid;
    grid-template-columns: repeat(9, 1fr);
    border: solid 1px black;
    max-width: 620px;
}
.grid span{
  border: solid .5px gray;
  background-color: khaki;
  text-align: center;
  width: 100%;
}
</style>
