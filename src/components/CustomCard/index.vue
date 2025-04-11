<template>
  <el-card :class="['custom-card', customClass]" :shadow="shadow">
    <div class="card-header">
      <h3>{{ title }}</h3>
      <!-- 插槽：头部操作区 -->
      <div class="header-actions">
        <slot name="header-actions"></slot>
      </div>
    </div>
    <div class="card-content">
      <slot>{{ content }}</slot>
    </div>
    <!-- 插槽：底部操作区 -->
    <div class="card-footer" v-if="$slots.footer">
      <slot name="footer"></slot>
    </div>
  </el-card>
</template>

<script>
export default {
  name: 'CustomCard',
  props: {
    title: {type: String, required: true},
    content: {type: String, default: ''},
    shadow: {type: String, default: 'always'}, // 控制阴影：always / hover / never
    customClass: {type: String, default: ''}, // 自定义 class
  },
};
</script>

<style scoped>
.custom-card {
  border-radius: 6px;
  overflow: hidden;
}

.card-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 12px;
}

.card-header h3 {
  margin: 0;
  font-size: 18px;
  font-weight: 600;
}

.card-content {
  margin-bottom: 12px;
  font-size: 14px;
  color: #606266;
}

.card-footer {
  text-align: right;
  border-top: 1px solid #ebeef5;
  padding-top: 12px;
  margin-top: 12px;
}
</style>
