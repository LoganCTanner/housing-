<!--
    need to reset arrow to false when not open
    idea:
        add prop of currentlyOpen,
        in span :class change {open: open} to {open: title === isOpened}

 -->
<script lang="ts">
import {defineComponent} from 'vue'
export default defineComponent({
    props: {
        title: String,
        currentlyOpen: String,
        open: {
            type: Boolean, 
            required:true,
            default:false}
    },
    

    methods: {
        toggle() {
            this.$emit('toggled', !this.open)
            
        }
    }
})
</script>

<!-- -->
<template>
    
    <div class="nav-button"
        @click="toggle">
        <div class="title">
            {{ title }} 
            <span :class=" { arrow: true, open: open }">
                &#10157;
            </span>
        </div>
    </div>

</template>

<!-- -->
<style scoped>
    .nav-button{
        background-color: white;
        height: 100%;
        
        
        color: black;
        background-color: #d3e4ff;
        border-color: #0063FF ;
        
        border-radius: 10px;
        border-style: solid;
        border-width: 1px;

        display: grid;
        place-items: center;
    }
    .title {
        text-align: center;
        line-height: 18px;
        
         
    }

    .title .arrow {
        display:inline-block;
        transform:rotate(-90deg);
        
    }
    .arrow {
        
        margin-bottom:2px;
        vertical-align: middle;
        text-align: center;
    }
    .title .arrow.open {
        transform:rotate(90deg);
    }

</style>