<template>
    <div class="row">
        <draggable :list="list" group="a" item-key="id" class="draggable-container">
            <template #item="{ element }">
                <CellComponent :id="element.id" :title="element.title" :width="element.width" :color="element.color"
                    :cellData="element" :onCellDrag="handleCellDrag" />
            </template>
        </draggable>

        <draggable :list="list2" group="a" item-key="id" class="draggable-container">
            <template #item="{ element }">
                <CellComponent :id="element.id" :title="element.title" :width="element.width" :color="element.color"
                    :cellData="element" :onCellDrag="handleCellDrag" />
            </template>
        </draggable>
        <draggable :list="list3" group="a" item-key="id" class="draggable-container">
            <template #item="{ element }">
                <CellComponent :id="element.id" :title="element.title" :width="element.width" :color="element.color"
                    :cellData="element" :onCellDrag="handleCellDrag" />
            </template>
        </draggable>
    </div>
</template>
  
<script>
import draggable from "vuedraggable";
import CellComponent from "./CellComponent.vue";
export default {
    components: {
        draggable,
        CellComponent
    },
    data() {
        return {
            list: [
                { id: "1", title: "Q", width: 40, color: "lightblue" },
                { id: "2", title: "W", width: 40, color: "lightblue" },
                { id: "3", title: "E", width: 40, color: "lightblue" },
                { id: "4", title: "R", width: 40, color: "lightblue" },
                { id: "5", title: "T", width: 40, color: "lightblue" },
                { id: "6", title: "Y", width: 40, color: "lightblue" },
                { id: "7", title: "U", width: 40, color: "lightblue" },
                { id: "8", title: "I", width: 40, color: "lightblue" },
                { id: "9", title: "O", width: 40, color: "lightblue" },
                { id: "10", title: "P", width: 40, color: "lightblue" },
            ],
            list2: [
                { id: "11", title: "A", width: 40, color: "lightgreen" },
                { id: "12", title: "S", width: 40, color: "lightgreen" },
                { id: "13", title: "D", width: 40, color: "lightgreen" },
                { id: "14", title: "F", width: 40, color: "lightgreen" },
                { id: "15", title: "G", width: 40, color: "lightgreen" },
                { id: "16", title: "H", width: 40, color: "lightgreen" },
                { id: "17", title: "J", width: 40, color: "lightgreen" },
                { id: "18", title: "K", width: 40, color: "lightgreen" },
                { id: "19", title: "L", width: 40, color: "lightgreen" },
                { id: "20", title: "Ç", width: 40, color: "lightgreen" },

            ],
            list3: [
                { id: "21", title: "Z", width: 40, color: "red" },
                { id: "22", title: "X", width: 40, color: "red" },
                { id: "23", title: "C", width: 40, color: "red" },
                { id: "24", title: "V", width: 40, color: "red" },
                { id: "25", title: "B", width: 40, color: "red" },
                { id: "26", title: "N", width: 40, color: "red" },
                { id: "27", title: "M", width: 40, color: "red" },
                { id: "28", title: "K", width: 40, color: "red" },
                { id: "29", title: ",", width: 40, color: "red" },
                { id: "30", title: ".", width: 40, color: "red" }
            ],
        };

    },
    methods: {
        handleCellDrag(cell) {
            // Handle the cell drag event here
            console.log('Cell dragged:', cell);
        },
    }
};
</script>
<style scoped>
.draggable-container {
    display: flex;
    flex-direction: row;
}
</style>