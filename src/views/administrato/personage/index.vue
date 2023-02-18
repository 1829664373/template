<template>
  <div class="app-container">
    角色
    <table-list :columns="columns" :list="list" :listLoading="listLoading" />
  </div>
</template>

<script>
import TableList from '@/components/TableList'
export default {
  data() {
    return {
      columns: [{
        label: '角色名称'
      }, {
        label: '角色类型'
      }, {
        label: '角色属性'
      }, {
        label: '角色储物'
      }, {
        label: '游戏技能'
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

