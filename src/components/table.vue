<template>
  <el-table
    :data="tableData"
    border
    stripe
    style="width: 100%">
    <el-table-column
      type="index"
      width="50">
    </el-table-column>
    <el-table-column
      prop="title"
      label="文章标题">
    </el-table-column>
    <el-table-column
      prop="author"
      label="作者"
      width="180">
    </el-table-column>
    <el-table-column
      prop="date"
      label="日期"
      width="180">
    </el-table-column>
    <el-table-column label="操作">
      <template slot-scope="scope">
        <el-button
          size="mini"
          @click="handleEdit(scope.$index, scope.row)">编辑</el-button>
        <el-button
          size="mini"
          type="danger"
          @click="handleDelete(scope.$index, scope.row)">删除</el-button>
      </template>
    </el-table-column>
  </el-table>
</template>

<script>
export default {
  name: 'table',
  data () {
    return {
      tableData: [{
        title: 'my first pape1',
        author: 'Alice',
        date: '2016-05-02'
      },
      {
        title: 'my second pape2',
        author: 'Bob',
        date: '2016-06-02'
      },
      {
        title: 'my third paper3',
        author: 'Cindy',
        date: '2016-12-02'
      }]
    }
  }
}
</script>

<style scoped>

</style>
