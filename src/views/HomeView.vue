<template>
  <div class="content">
    <!-- 全屏容器 -->
    <dv-full-screen-container>
      <!-- 标题 -->
      <ModuleTitle />
      <!-- 第二行 -->
      <ModuleMain />
      <!-- 第三行 -->
      <ModuleThird />
    </dv-full-screen-container>
  </div>
</template>

<script>
import ModuleTitle from './moduleTitle.vue';
import ModuleMain from './moduleMain.vue';
import ModuleThird from './moduleThird.vue';

export default {
  name: 'HomeView',
  components: {
    ModuleTitle,
    ModuleMain,
    ModuleThird
  },
  data() {
    return {
    } 
  } 
}
</script>