<script lang="ts">

import Tag from './Tag.vue';  
   export default {
     components: { Tag },
       props: {
          ingrediente: { type: String, required: true }
       },
       data() {
          return {
             selected: false
          }
       },
   }
</script>

<template>
   <button class="ingrediente" @:click="selected = !selected" :aria-pressed="selected">
      <Tag :texto="ingrediente"  :active="selected"/>
   </button>
</template>

<style scoped>
   .ingrediente {
      border: none;
      background: none;
      cursor: pointer;
   }
</style>
