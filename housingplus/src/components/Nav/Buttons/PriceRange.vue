<!-- -->
<script lang="ts">
import {defineComponent} from 'vue'
import NavButton from './NavButton.vue'
import PriceRangeMenu from './Menus/PriceRangeMenu.vue'

export default defineComponent({
    components: { NavButton, PriceRangeMenu },
    props: {
        currentlyOpen: String
    },
    data: () =>({
        name: 'PriceRange',
    }),
    computed: {
        opened() {
            return this.currentlyOpen === this.name
        }
    },
    methods: {
        toggled(isOpen:boolean){
            this.$emit('open', isOpen, this.name)
        }
    }
})
</script>

<!-- -->
<template>
    <div class="PriceRangeButton">
        <NavButton 
        title="Price Range"
        currentlyOpen = "currentlyOpen"
        :open="opened"
        @toggled="toggled"/>

        <div v-show="opened">
            <PriceRangeMenu />
        </div>
    </div>
</template>

<!-- -->
<style scoped>
.PriceRangeButton{
    width: 163px;
    height:100%;
}


</style>