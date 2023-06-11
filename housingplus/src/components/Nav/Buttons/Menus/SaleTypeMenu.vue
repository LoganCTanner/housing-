<!-- -->
<script lang="ts">
import {defineComponent} from 'vue'
import Radio from '../Radio.vue'
export default defineComponent({
    components: {Radio},
    data: () => ({
        selected: 'For Sale',
        forSale: 'For Sale',
        forRent: 'For Rent',
    }),
    methods: {
        clicked(name:string){
            this.selected = name
        }
    }
    

})
</script>

<!-- -->
<template>

    <div class="SaleTypeMenu">
        <div 
            :class="forSale"
            @click="clicked(forSale)">
            <Radio :isSelected="selected === forSale"/>
            <p>{{ forSale }}</p>
        </div>
        <div 
            :class="forRent"
            @click="clicked(forRent)">
            <Radio :isSelected="selected === forRent"/>
            <p>{{ forRent }}</p>
        </div>
    </div>
    
</template>

<!-- -->
<style scoped>
.SaleTypeMenu {
    height: 100px;
    width: 250px;

    background-color: wheat;

    display: grid;
    align-items: center;
}

.ForRent {
    margin-top:10px;    
}

.ForRent, .ForSale {
    display: float;
}

</style>