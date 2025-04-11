<template>
  <CustomElCard>
    <h3>{{ title }}</h3>
    <video v-if="type === 'video'" controls :src="src" class="media"></video>
    <audio v-if="type === 'audio'" controls :src="src" class="media"></audio>
    <p>{{ description }}</p>
  </CustomElCard>
</template>

<script setup>
import CustomElCard from "@/components/CustomElCard/index.vue";

defineOptions({
  name: 'MediaCard'
})

const props = defineProps({
  title: {type: String, required: true},
  type: {type: String, required: true}, // 'video' or 'audio'
  src: {type: String, required: true},
  description: {type: String, default: ''},
});

</script>

<style scoped>
.media {
  width: 100%;
  margin-top: 10px;
}
</style>
