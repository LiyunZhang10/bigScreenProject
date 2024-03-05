<template>
  <div class="module-box ">
    <!-- 左 -->
    <div style="flex:0 1 25%">
      <dv-border-box-1 style="width:100%;height:150px;">
        <CapsuleChart :dataChart="dataChart" :colorsChart="['#e062ae', '#fb7293', '#e690d1', '#32c5e9', '#96bfff']" />
      </dv-border-box-1>
      <dv-border-box-2 style="width:100%;height:150px;">
        <dv-water-level-pond :config="config3" style="width:100%;height:100%" />
      </dv-border-box-2>
      <dv-border-box-10 style="width:100%;height:150px;">
        dv-border-box-3
      </dv-border-box-10>
    </div>
    <!-- 中 -->
    <div style="flex:0 1 50%">
      <dv-border-box-9 style="width:100%;height:450px;">
        <dv-flyline-chart :config="config4" style="width:100%;height:100%;" />
      </dv-border-box-9>
    </div>
    <!-- 右 -->
    <div style="flex:0 1 25%">
      <dv-border-box-8 style="width:100%;height:225px;">
        <dv-capsule-chart :config="config2" style="width:100%;height:100%" />
      </dv-border-box-8> 
      <dv-border-box-10 style="width:100%;height:225px;">
        <CapsuleChart />
      </dv-border-box-10>
    </div>
  </div>
</template>
<script>
import CapsuleChart from './capsuleChart.vue';

export default {
  components: {
    CapsuleChart
  },
  data() {
    return {
      dataChart: [
        {name:"标题1",value:100},
        {name:"标题2",value:100},
        {name:"标题3",value:40},
        {name:"标题4",value:320},
        {name:"标题5",value:100},
        {name:"标题6",value:100}
      ],
      config2: {
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
            value: 66
          },
        ],
      },
      config3: {
        data: [66, 45],
        shape: 'roundRect',
        colors: ['#f60', 'green'],
        waveOpacity: 0.2,
      },
      config4: {
        centerPoint: [0.48, 0.35],
        points: [
          [0.52, 0.23],
          [0.43, 0.29],
          [0.59, 0.35],
          [0.53, 0.47],
          [0.45, 0.54],
          [0.36, 0.38],
          [0.62, 0.55],
          [0.56, 0.56],
          [0.37, 0.66],
          [0.55, 0.81],
          [0.55, 0.67],
          [0.37, 0.29],
          [0.20, 0.36],
          [0.76, 0.41],
          [0.59, 0.18],
          [0.68, 0.17],
          [0.59, 0.10]
        ],
        bgImgUrl: require('../assets/img/map.jpg'),
        flylineColor: ['black']
      }
    }
  }
} 
</script>