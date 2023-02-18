<template>
  <div class="app-container">
    游戏
    <table-list :columns="columns" :list="list" :listLoading="listLoading" />
  </div>
</template>

<script>
import TableList from '@/components/TableList'
export default {
  data() {
    return {
      columns: [{
        label: '游戏名称'
      }, {
        label: '游戏详情'
      }, {
        label: '游戏类型'
      }, {
        label: '游戏地图'
      }, {
        label: '游戏角色'
      }, {
        label: '游戏技能'
      }, {
        label: '游戏物品'
      }],
      list: null,
      listLoading: true
    }
  },
  components: {
    TableList
  },
  watch: {
  },
  created() {
    this.listLoading = false
  },
  methods: {
  }
}
</script>

