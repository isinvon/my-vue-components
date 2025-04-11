<template>
  <CustomElCard>
    <h3>{{ title }}</h3>
    <el-progress
        v-for="(item, index) in progressData"
        :key="index"
        :text-inside="true"
        :stroke-width="18"
        :percentage="item.percentage"
        :color="item.color"
        style="margin-bottom: 10px;"
    />
  </CustomElCard>
</template>

<script setup>
import CustomElCard from "@/components/CustomElCard/index.vue";

defineOptions({
  name: 'ProgressCard'
})

const props = defineProps({
  title: {type: String, required: true},
  progressData: {type: Array, required: true},
})
</script>

<style scoped>
</style>
