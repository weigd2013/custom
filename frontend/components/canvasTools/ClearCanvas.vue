<template>
  <div></div>
</template>

<script>
import customEvents from '~/utils/customEvents';

export default {
  props: {
    canvas: {
      type: Object,
      required: true,
    },
  },
  mounted() {
    console.log("clearcanvas");
    console.log(customEvents.canvasTools.CanvasClear);
    this.$nuxt.$on(customEvents.canvasTools.CanvasClear, () => {
      console.log("customEvents.canvasTools.CanvasClear");
      console.log("customEvents.canvasTools.CanvasClear");
      this.clearCanvas();
    });
  },
  methods: {
    clearCanvas() {
      this.canvas.clear();
    },
  },
};
</script>
