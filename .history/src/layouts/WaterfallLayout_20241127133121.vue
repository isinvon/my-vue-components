<!--竖着-->
<!--<template>-->
<!--  <div class="waterfall-layout">-->
<!--    <slot/>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--export default {-->
<!--  name: 'WaterfallLayout',-->
<!--};-->
<!--</script>-->

<!--<style scoped>-->
<!--.waterfall-layout {-->
<!--  display: grid; /* 使用 CSS Grid 布局 */-->
<!--  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); /* 动态列数 */-->
<!--  gap: 20px; /* 卡片间距 */-->
<!--  width: 100%;-->
<!--}-->
<!--</style>-->

<!--横着-->
<template>
  <div class="waterfall-layout">
    <slot />
  </div>
</template>

<script>
export default {
  name: 'WaterfallLayout',
};
</script>

<style lang="less" scoped>
.waterfall-layout {
  column-count: 5; /* 定义列数 */
  column-gap: 20px; /* 列之间的间距 */
  width: 100%;
}

.waterfall-layout > * {
  break-inside: avoid; /* 防止子元素被拆分到不同列 */
  margin-bottom: 20px; /* 卡片之间的间距 */
}
</style>
