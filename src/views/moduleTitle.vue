<template>
  <div class="module-box ">
    <div style="flex:0 1 30%">
      <dv-decoration-10 style="height:5px;" />
    </div>
    <div style="flex:0 1 40%">
      <div class="d-flex">
      <!-- 左 -->
      <dv-decoration-8  style="height:50px; flex:1;" />
      <!-- 中 -->
      <div class="tc box-middle" style="flex:1;">智慧工厂数据中心</div>
      <!-- 右 -->
      <dv-decoration-8 :reverse="true" style="height:50px; flex:1;" />
      </div>
    </div>
    <div style="flex:0 1 30%">
      <dv-decoration-10 style="height:5px; transform :rotateY(180deg);" />
    </div>
  </div>
</template>