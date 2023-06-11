<!-- -->
<script lang="ts">
import {defineComponent} from 'vue'
import NavButton from './NavButton.vue'
export default defineComponent({
    components: { NavButton },
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

        <div v-if="opened">
            <div class="PriceRangeMenu"></div>
        </div>
    </div>
</template>

<!-- -->
<style scoped>
.PriceRangeButton{
    width: 163px;
    height:100%;
}

.PriceRangeMenu {
        width: 150px;
        height: 225px;

        background-color: wheat;
        margin-top: 5px;
}
</style>