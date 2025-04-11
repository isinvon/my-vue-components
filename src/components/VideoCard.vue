<template>
  <CustomElCard>
    <div class="video-card">
      <video controls>
        <source :src="videoSrc" type="video/mp4">
        Your browser does not support the video tag.
      </video>
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
    </div>
  </CustomElCard>
</template>

<script setup>
import CustomElCard from '@/components/CustomElCard/index.vue'

defineProps({
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  },
  videoSrc: {
    type: String,
    required: true
  }
});
</script>

<style scoped>
.video-card {
  border: 1px solid #ccc;
  padding: 15px;
  margin: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  background-color: #fff;
  border-radius: 8px;
  transition: transform 0.2s;
}

.video-card video {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.video-card:hover {
  transform: translateY(-5px);
}
</style>