<!-- -->
<script lang="ts">
import {defineComponent} from 'vue'
export default defineComponent({

})
</script>

<!-- -->
<template>
    <div class="PriceRangeMenu">
        <div class="titleBackground">
            <div class="title">Price Range</div>
        </div>
        <div class="background">
        </div>
    </div>
    
</template>

<!-- -->
<style scoped>
.PriceRangeMenu {
    height: 140px;
    width: 375px;

    background-color: wheat;

    border-radius: 7px;
    
    margin-left:-115px;
    margin-top: 10px;

    filter: drop-shadow(0px 3px 5px rgba(0,0,0,.2));
}

.titleBackground {
    height: 25px;
    width: 100%;

    background-color: darkgray;

    border-top-left-radius: 7px;
    border-top-right-radius: 7px;

    align-content: center;

    
}

.title {
    color: white;

    padding-top: 3px;
    padding-left: 3px;

}


</style>