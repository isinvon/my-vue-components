<template>
  <CustomElCard>
    <img :src="avatar" alt="Avatar" class="avatar"/>
    <h3>{{ name }}</h3>
    <p>{{ bio }}</p>
  </CustomElCard>
</template>

<script setup>
import CustomElCard from "@/components/CustomElCard/index.vue";

defineOptions({
  name: "ProfileCard"
})
const props = defineProps({
  name: {type: String, required: true},
  bio: {type: String, default: ''},
  avatar: {
    type: String,
    required: true,
    default: 'https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png'
  },
})
</script>

<style scoped>
.avatar {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  margin-bottom: 10px;
}
</style>
