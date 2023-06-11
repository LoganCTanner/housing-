<!-- -->
<sciprt lang="ts">
    import { defineComponent } from 'vue'
    export default defineComponent({
        });

</sciprt>

<!-- -->
<template>
    <div class="Selected">
    </div>
    <div class="Unselected">
    </div>
</template>

<!-- -->
<style scoped>
.Unselected {
    height: 10rem;
    width: 10rem;

    background-color: #F0F0F0;
    border-color: #6e6e6e;
    
    border-radius: 1rem;
    border-width: 2.5rem;
    border-style:solid; 
}

.Selected {
    height:10rem;
    width:10rem;
    
    background-color: #d3e4ff;
    border-color: #0063FF ;
    
    border-radius:1rem;
    border-width:2.5rem;
    border-style:solid;
}

</style>