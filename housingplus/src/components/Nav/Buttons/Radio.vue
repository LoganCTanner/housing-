<!-- -->
<script lang="ts">
import {defineComponent} from 'vue'
export default defineComponent({
    props: {
        isSelected: Boolean
    },



})
</script>

<!-- -->
<template>
    <div 
    :class="{
        radio: true, 
        selected: isSelected
    }">
    </div>
    
</template>

<!-- -->
<style scoped>
.radio{
    height:25px;
    width:25px;

    background-color: grey;
    border-color: yellow;

    border-radius: 25px;
    border-width: 10px;
    border-style:solid;
}
.selected {
    background-color:blue;
    border-color:yellow;
}

</style>