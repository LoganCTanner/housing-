<!-- -->
<script lang="ts">
    import { defineComponent } from 'vue'
    import SaleType from './Buttons/SaleType.vue'
    import PriceRange from './Buttons/PriceRange.vue'
    import Locations from './Buttons/Locations.vue'
    import Checkbox from './Buttons/Checkbox.vue'
    import NavButton from './Buttons/NavButton.vue'

    export default defineComponent({
        components: {SaleType, PriceRange,Locations},
        data: () => ({
            currentlyOpen: ''
        }),
        methods: {
            open(isOpen: boolean, name: string){
                if(isOpen) {
                    this.currentlyOpen = name
                }
                else if(name === this.currentlyOpen){
                    this.currentlyOpen = ''
                }
            }
        }

    });
</script>

<!-- -->
<template>
    <nav class="Nav">
        <SaleType @open="open" :currentlyOpen="currentlyOpen"/>
        <PriceRange @open="open" :currentlyOpen="currentlyOpen"/>
        <Locations @open="open" :currentlyOpen="currentlyOpen"/>
   
    </nav>
</template>

<!-- -->
<style scoped>
    .Nav {
        height: 44px;
        display: flex;
        
        justify-items: stretch;
        align-items: stretch;
        column-gap:6px;
    }


</style>