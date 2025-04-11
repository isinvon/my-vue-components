<template>
  <CustomElCard>
    <blockquote>
      <p>{{ quote }}</p>
      <footer>— {{ author }}</footer>
    </blockquote>
  </CustomElCard>
</template>

<script setup>
import CustomElCard from "@/components/CustomElCard/index.vue";

defineOptions({
  name: 'QuoteCard',
})

const props = defineProps({
  quote: {type: String, required: true},
  author: {type: String, required: true},
})

</script>

<style scoped>
blockquote {
  font-style: italic;
  border-left: 5px solid #ddd;
  padding-left: 10px;
}

footer {
  text-align: right;
  font-weight: bold;
}
</style>
