<!-- -->
<script lang="ts">
import {defineComponent} from 'vue'
import NavButton from './NavButton.vue'
import SaleTypeMenu from './Menus/SaleTypeMenu.vue'
export default defineComponent({
    components: { NavButton, SaleTypeMenu },
    props: {
        currentlyOpen: String
    },
    data: () =>({
        name: 'SaleType',
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

    <div class="SaleTypeButton">
        <NavButton 
        title="Sale Type" 
        currentlyOpen = "currentlyOpen"
        :open="opened"
        @toggled="toggled"/>

        <div v-show="opened">
            <SaleTypeMenu />
        </div>

    </div>
    
</template>

<!--
    portrait:
    123px w, 44px h

    landscape:
    131 px w, 44px h

 -->
<style scoped>
    .SaleTypeButton{
        width:131px;
        height: 100%
    }


</style>