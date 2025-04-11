<template>
  <WaterfallLayout>
    <SimpleCard title="示例标题" content="简单卡片内容"/>
    <CodeCard title="代码示例" code="console.log('Hello World');"/>
    <ImageCard src="/path/to/image.jpg" description="示例图片"/>
    <QuoteCard quote="天行健，君子以自强不息。" author="《周易》"/>
    <SimpleCard title="示例标题" content="简单卡片内容"/>
    <ProfileCard avatar="/path/to/avatar.jpg" name="张三" bio="前端开发者"/>
    <StatsCard title="项目统计" :stats="{ Likes: 123, Stars: 456, Forks: 78 }"/>
    <TagCard title="标签集合"
             :tags="[{ label: 'Vue', type: 'success' }, { label: 'JavaScript', type: 'info' }, { label: 'Element Plus', type: 'warning' }]"/>
    <TimelineCard title="项目时间轴"
                  :events="[{ timestamp: '2024-01-01', content: '项目启动' }, { timestamp: '2024-06-01', content: '第一阶段完成', color: 'green' }, { timestamp: '2024-12-31', content: '项目交付', color: 'red' }]"/>
    <MediaCard title="示例视频" type="video" src="/path/to/video.mp4" description="项目演示视频"/>
    <ProgressCard title="任务进度"
                  :progressData="[{ percentage: 70, color: '#409eff' }, { percentage: 45, color: '#67c23a' }]"/>
    <DisclaimerCard/>
    <DisclaimerCard_v2/>
    <DisclaimerCard_v3/>
    <DisclaimerCard_v4/>
    <DisclaimerCard_v5/>
    <DisclaimerCard_v6/>
    <DisclaimerCard_v7/>
  </WaterfallLayout>
</template>

<script setup>
import {inject} from "vue";

import WaterfallLayout from './layouts/WaterfallLayout.vue';
import SimpleCard from '@/components/SimpleCard.vue';
import CodeCard from '@/components/CodeCard.vue';
import ImageCard from '@/components/ImageCard.vue';
import QuoteCard from '@/components/QuoteCard.vue';
import ProfileCard from '@/components/ProfileCard.vue';
import StatsCard from '@/components/StatsCard.vue';
import TagCard from '@/components/TagCard.vue';
import TimelineCard from '@/components/TimelineCard.vue';
import MediaCard from '@/components/MediaCard.vue';
import ProgressCard from '@/components/ProgressCard.vue';
import DisclaimerCard from '@/components/DisclaimerCard.vue';
import DisclaimerCard_v2 from "@/components/DisclaimerCard_v2.vue";
import DisclaimerCard_v3 from "@/components/DisclaimerCard_v3.vue";
import DisclaimerCard_v4 from "@/components/DisclaimerCard_v4.vue";
import DisclaimerCard_v5 from "@/components/DisclaimerCard_v5.vue";
import DisclaimerCard_v6 from "@/components/DisclaimerCard_v6.vue";
import DisclaimerCard_v7 from "@/components/DisclaimerCard_v7.vue";

const componentCodes = inject('componentCodes');
</script>

<style>
/* 全局样式优化 */
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f5f5f5;
  padding: 20px;
}

</style>

