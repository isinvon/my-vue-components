<template>
  <CustomElCard>
    <img :src="src" :alt="alt"/>
    <p>{{ description }}</p>
  </CustomElCard>
</template>

<script setup>
import CustomElCard from "@/components/CustomElCard/index.vue";

defineOptions({
  name: 'ImageCard',
})
const props = defineProps({
  src: {type: String, required: true},
  alt: {type: String, default: ''},
  description: {type: String, default: ''},
})

</script>

<style scoped>
img {
  max-width: 100%;
  height: auto;
  border-radius: 4px;
}
</style>
