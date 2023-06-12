<!-- -->
<script lang="ts">
import {defineComponent} from 'vue'
import Radio from '../Radio.vue'
import { propsToAttrMap } from '@vue/shared';
export default defineComponent({
    components: {Radio},
    props: {
        previousSelection: String,
    },
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
        <div class="title">
            <div class="name">Sale Type</div>
            
        </div>
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
    height: 125px;
    width: 175px;
    
    margin-top: 10px;

    background-color: wheat;

    display: grid;
    align-items: center;

    filter: drop-shadow(0px 3px 5px rgba(0,0,0,.2));
    border-radius:7px;

}

.title{
    height: 25px;
    width: 100%;

    background-color: darkgray;
    border-top-left-radius: 7px;
    border-top-right-radius: 7px;
}

.name{
    margin-top:3px;
    margin-left:3px;
    color:white
}

.ForRent {
    margin-top:10px;    
}

p {
    margin-left:50px;
    margin-top:-31px
}

</style>
