<template>
  <div ref="chart" style="width: 100%;height: 400px;"></div>
</template>

<script>
import * as echarts from 'echarts/core';
export default {
  props: {
    typeChart: {
      type: String,
      default: 'line'
    }
  },
  data() {
    return {
      lists:[], // 存放数据
    }
  },
  mounted() {
    this.initWebsocket(); // 初始化websocket
  },
  methods: {
    initChart() {
      // 基于准备好的dom，初始化echarts实例
      var myChart = echarts.init(this.$refs.chart);

      // 指定图表的配置项和数据
      var option = {
        xAxis: {
          type: 'category',
          data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
        },
        yAxis: {
          type: 'value'
        },
        series: [
          {
            data: this.lists,
            type: this.typeChart,
            smooth: true
          }
        ]
      };
      myChart.setOption(option);
    },
  
    initWebsocket() {
      // 初始化websocket
      const ws = new WebSocket("ws://10.252.74.230:8080");
      // 连接成功
      ws.onopen = function () {
        alert("WebSocket连接成功")
      };
      // 连接失败
      ws.onerror = function () {
        alert("WebSocket连接失败")
      };
      // 接收消息
      ws.onmessage = msg => {
        console.log(msg);
        let res = JSON.parse(msg.data);
        this.lists = res.message;
        this.initChart();
      }
    }
  }
}
</script>
