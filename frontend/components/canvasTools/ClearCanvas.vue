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
    this.$nuxt.$on(customEvents.canvasTools.clearCanvas, () => {
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
