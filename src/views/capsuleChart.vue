<template>
  <!-- 胶囊柱图 -->
  <dv-capsule-chart :config="config" style="width:100%;height:200px" />
</template>

<script>
export default {
  props: {
    colorsChart: {
      type: Array,
      default: () => []
    },
    dataChart: {
      type: Array,
      default: () => [
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
      ]
    }
  },

  data() {
    return {
      config: {
        data: this.dataChart,
        colors: this.colorsChart,
        unit: '单位',
        showValue: true
      }
    }
  }
}
</script>