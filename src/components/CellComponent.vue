<template>
    <div
      :id="id"
      :style="{ width: width + 'px', backgroundColor: color }"
      class="cell"
      draggable="true"
      @dragstart="dragStart"
    >
      {{ title }}
    </div>
  </template>
  
  <script>
  export default {
    props: {
      id: {
        type: String,
        required: true,
      },
      title: {
        type: String,
        required: true,
      },
      width: {
        type: Number,
        required: true,
      },
      color: {
        type: String,
        required: true,
      },
      cellData: {
        type: Object,
        required: true,
      },
      onCellDrag: {
        type: Function,
        required: false,
      },
    },
    methods: {
      dragStart(event) {
        event.dataTransfer.setData('text/plain', this.id);
        this.onCellDrag(this.cellData);
      },
    },
  };
  </script>
  
  <style scoped>
  .cell {
    border: 1px solid #ccc;
    padding: 10px;
    cursor: move;
  }
  </style>
  