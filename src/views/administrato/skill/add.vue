<template>
  <div class="app-container">
    <div>技能</div>
    <el-button class="add-button" type="primary" @click="onSubmit">新增</el-button>
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
      this.$store.dispatch('tagsView/delView', this.$route).then(({ visitedViews }) => {
        this.$router.replace({ path: "/administrato/skill" });
      })
    },
  }
}
</script>
<style scoped>
.add-button {
  padding-top: 10px;
}
</style>

