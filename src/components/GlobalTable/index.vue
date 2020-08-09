<template>
  <el-table :data="tableData" style="width: 100%" @selection-change="handleSelectionChange">
    <el-table-column
      v-for="(item,i) in tableColumu"
      :key="i"
      :label="item.label"
      :prop="item.field"
      :min-width="item.width"
      :formatter="formatterParmas"
      show-overflow-tooltip
    />
  </el-table>
</template>

<script>
export default {
  name: 'GlobalTable',
  components: {},
  props: {
    tableData: {
      // 表格数据
      type: Array,
      default() {
        return []
      }
    },
    tableColumu: {
      // 表格列数据
      type: Array,
      default() {
        return []
      }
    },
    tableOption: {
      // 表格属性
      type: Object,
      default: null
    }
  }
}
</script>

<style>
</style>
