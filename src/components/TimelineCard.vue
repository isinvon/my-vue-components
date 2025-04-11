<template>
  <CustomElCard>
    <h3>{{ title }}</h3>
    <el-timeline>
      <el-timeline-item
          v-for="(event, index) in events"
          :key="index"
          :timestamp="event.timestamp"
          :color="event.color || 'blue'"
      >
        {{ event.content }}
      </el-timeline-item>
    </el-timeline>
  </CustomElCard>
</template>

<script setup>
import CustomElCard from "@/components/CustomElCard/index.vue";

defineOptions({
  name: 'TimelineCard'
})

const props = defineProps({
  title: {type: String, required: true},
  events: {
    type: Array,
    required: true,
    default: () => [],
  },
})
</script>

<style scoped>
</style>
