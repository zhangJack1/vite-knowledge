

<template>
    <f-space>
      <f-button type="primary" @click="onShow('left')">介绍</f-button>
    </f-space>
  
    <f-drawer v-model:visible="visible1" title="古诗名篇" :direction="direction">
      <h3>沁园春·雪</h3>
  
      <p>北国风光，千里冰封，万里雪飘。</p>
      <p>望长城内外，惟余莽莽；大河上下，顿失滔滔。</p>
      <p>山舞银蛇，原驰蜡象，欲与天公试比高。</p>
      <p>须晴日，看红装素裹，分外妖娆。</p>
  
      <br />
  
      <p>江山如此多娇，引无数英雄竞折腰。</p>
      <p>惜秦皇汉武，略输文采；唐宗宋祖，稍逊风骚。</p>
      <p>一代天骄，成吉思汗，只识弯弓射大雕。</p>
      <p>俱往矣，数风流人物，还看今朝。</p>

      <Video
    src="/lol.mp4"
    :width="300"
    :height="200"
    :second="3" 
    />
    </f-drawer>
  </template>
  
  <script lang="ts" setup>
    import { ref } from 'vue'
    import type { DrawerDirection } from 'fighting-design'
    import { fold } from '../untils/types'
  
    const visible1 = ref(false)
    const direction = ref<DrawerDirection>('right')
  
    const onShow = (dir: DrawerDirection): void => {
      direction.value = dir
      visible1.value = true
    }
  </script>


