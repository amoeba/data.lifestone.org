<script type="ts">
export default {
  data() {
    const width = 16;
    const dim = 4;
    const tile_width = width / dim;
    const base_color = "0, 170, 255"; // r, g, b

    const tiles = [...Array(dim * dim).keys()].map(i => {
      return {
        i: i,
        x: tile_width * (i % dim),
        y: tile_width * (Math.floor(i / dim)),
        color: "rgba(" + base_color + "," + Math.random() + ")"
      }
    });

    return {
      width: width,
      viewBox: "0 0 " + width + " " + width,
      tile_width: tile_width,
      height: 10,
      tiles: tiles
    };
  }
}
</script>

<template>
  <svg :width="width" :height="width" :viewBox="viewBox" xmlns="http://www.w3.org/2000/svg">
    <rect v-for="tile in tiles" :v-key="tile.i" :x="tile.x" :y="tile.y" :width="tile_width" :height="tile_width"
      :fill="tile.color" />
  </svg>
</template>
