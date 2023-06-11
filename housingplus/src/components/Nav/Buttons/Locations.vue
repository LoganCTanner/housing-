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
        name: 'Locations'
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
    <div class="LocationsButton">
        <NavButton 
        title="Locations" 
        currentlyOpen = "currentlyOpen"
        :open="opened"
        @toggled="toggled"/>

        <div v-if="opened">
            <div class="LocationsMenu">

            </div>
        </div>
    </div>
    
</template>

<!-- -->
<style scoped>
    .LocationsButton{
        width: 120px;
        height:100%
    }
    .LocationsMenu {
        width: 150px;
        height: 225px;

        background-color: wheat;
        margin-top: 5px;
    }

</style>