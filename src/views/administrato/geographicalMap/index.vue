<template>
    <div class="app-container">
      地图
      <table-list :columns="columns" :list="list" :listLoading="listLoading" />
    </div>
  </template>
  
  <script>
  import TableList from '@/components/TableList'
  export default {
    data() {
      return {
        columns: [{
          label: '地图名称'
        }, {
          label: '地图详情'
        }, {
          label: '地图类型'
        }, {
          label: '游戏地图npc',
          width:115
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
  
  