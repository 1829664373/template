<template>
  <div class="app-container">
    <div>技能</div>

    <el-button class="add-button" size="small"  type="primary" @click="onSubmit">新增</el-button>
    <table-list :columns="columns" :list="list" :listLoading="listLoading" />
  </div>
</template>

<script>
import TableList from '@/components/TableList'
export default {
  data() {
    return {
      columns: [{
        label: '技能名称'
      }, {
        label: '技能类型'
      }, {
        label: '技能阶段'
      }, {
        label: '技能属性'
      }, {
        label: '技能克制'
      }, {
        label: '技能发动时长',
        width: 120
      }, {
        label: '技能时长'
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
    onSubmit() {
      this.$message('submit!')
      // 添加路由
      // this.$store.dispatch('/administrato', )
      this.$store.dispatch('tagsView/addView', {
        meta: {
          title: '新增'
        },
        name: '123',
        path: `/administrato/add/123`
      })
      // 跳转路由
      this.$router.push(`/administrato/add/123`)

    },
  }
}
</script>
<style scoped>
.add-button {
  margin-top: 10px;
}
</style>

