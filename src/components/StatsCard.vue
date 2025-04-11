<template>
  <CustomElCard>
    <h3>{{ title }}</h3>
    <div class="stats">
      <div v-for="(value, key) in stats" :key="key">
        <strong>{{ value }}</strong>
        <p>{{ key }}</p>
      </div>
    </div>
  </CustomElCard>
</template>


<script setup>

import CustomElCard from "@/components/CustomElCard/index.vue";

defineOptions({
  name: 'StatsCard',
})

const props = defineProps({
  title: {type: String, required: true},
  stats: {type: Object, required: true},
})
</script>

<style scoped>
.stats {
  display: flex;
  justify-content: space-around;
}

.stats div {
  text-align: center;
}
</style>
