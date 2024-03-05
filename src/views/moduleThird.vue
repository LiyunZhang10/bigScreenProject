<template>
  <!-- 第三行 -->
  <div class="module-box ">
    <div style="flex:0 1 50%">
      <dv-border-box-8 style="width:100%;height:300px;">
        <LineChart :typeChart="'bar'"/>
      </dv-border-box-8>
    </div>
    <div style="flex:0 1 25%">
      <dv-border-box-9 style="width:100%;height:300px;">
        <dv-capsule-chart :config="config1" style="width:100%;height:400px" />
      </dv-border-box-9>
    </div>
    <div style="flex:0 1 25%">
      <dv-border-box-10 style="width:100%;height:300px;">
        <dv-water-level-pond :config="config3" style="width:100%;height:400px" />
      </dv-border-box-10>
    </div>
  </div>  
</template>

<script>
import LineChart from "./lineChart.vue"

export default {
  components: {
    LineChart
  },
  data() {
    return {
      config1: {
        data: [
          {
            name: '南阳',
            value: 167
          },
          {
            name: '周口',
            value: 123
          },
          {
            name: '漯河',
            value: 98
          },
          {
            name: '郑州',
            value: 75
          },
          {
            name: '西峡',
            value: 55
          }
        ],
        colors: [
          '#FF6E6E',
          '#FFD86E',
          '#5B8FF9',
          '#5AD8A6',
          '#5D7092'
        ],
        unit: '单位',
        showValue: true
      }
    }
  }
}
</script>
