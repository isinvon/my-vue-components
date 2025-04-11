<template>
  <CustomElCard>
    <h3>{{ title }}</h3>
    <p>{{ content }}</p>
  </CustomElCard>
</template>

<script setup>
import CustomElCard from "@/components/CustomElCard/index.vue";

defineOptions({
  name: 'SimpleCard',
})
const props = defineProps({
  title: {type: String, required: true},
  content: {type: String, required: true},
})

</script>
