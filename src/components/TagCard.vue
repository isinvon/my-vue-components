<template>
  <CustomElCard>
    <h3>{{ title }}</h3>
    <el-tag
        v-for="(tag, index) in tags"
        :key="index"
        :type="tag.type || 'primary'"
        style="margin: 5px;"
    >
      {{ tag.label }}
    </el-tag>
  </CustomElCard>
</template>

<script setup>
import CustomElCard from "@/components/CustomElCard/index.vue";

defineOptions({
  name: 'TagCard',
})

const props = defineProps({
  title: {type: String, required: true},
  tags: {
    type: Array,
    required: true,
    default: () => [],
  },
})
</script>

<style scoped>
</style>
