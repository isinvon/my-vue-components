<template>
  <CustomElCard>
    <h3>{{ title }}</h3>
    <pre><code>{{ code }}</code></pre>
  </CustomElCard>
</template>

<script setup>
import CustomElCard from "@/components/CustomElCard/index.vue";

defineOptions({
  name: 'CodeCard',
})

const props = defineProps({
  title: {type: String, required: true},
  code: {type: String, required: true},
})

</script>

<style scoped>
pre {
  background: #f5f5f5;
  padding: 10px;
  border-radius: 4px;
  overflow-x: auto;
}
</style>
