<script  lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import {defineComponent} from 'vue'
import Nav from './components/Nav/Nav.vue'
import Checkbox from './components/Nav/Buttons/Checkbox.vue'
import SaleType from './components/Nav/Buttons/SaleType.vue'

export default defineComponent({
  components: {Nav}
})

//console.log(Object.keys(import.meta.env))



</script>

<template>
  
  <Nav/>
  
  <RouterView />
</template>

<style scoped>


</style>
