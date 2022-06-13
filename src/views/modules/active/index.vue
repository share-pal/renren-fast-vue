<template>
  <div>
    <el-descriptions :column="6">
      <el-descriptions-item label="平台总流量">182,120</el-descriptions-item>
      <el-descriptions-item label="注册用户">182,120</el-descriptions-item>
      <el-descriptions-item label="钱包用户">182,120</el-descriptions-item>
      <el-descriptions-item label="浏览用户">182,120</el-descriptions-item>
      <el-descriptions-item label="活跃用户">182,120</el-descriptions-item>
      <el-descriptions-item label="团队用户">182,120</el-descriptions-item>
    </el-descriptions>
    <div>
      <el-form>
        <el-row>
          <el-col :span="8">
            <el-form-item>
              <div style="width: 200px">
                <el-input
                  placeholder="搜索"
                  suffix-icon="el-input__icon el-icon-search"
                  v-model="form.value">
                </el-input>
              </div>
            </el-form-item>
          </el-col>
          <el-col :span="8"><div style="opacity: 0" class="grid-content bg-purple-light">11</div></el-col>
          <el-col :span="8">
            <div style="display:flex;justify-content: flex-end">
              <el-form-item>
                <el-select v-model="value" placeholder="请选择">
                  <el-option
                    v-for="item in options"
                    :key="item.value"
                    :label="item.label"
                    :value="item.value">
                  </el-option>
                </el-select>
              </el-form-item>
            </div>
          </el-col>
        </el-row>


      </el-form>
    </div>
    <div>
      <el-table
        :data="tableData"
        border
        style="width: 100%">
        <el-table-column
          fixed
          prop="date"
          label="日期"
          width="150">
        </el-table-column>
        <el-table-column
          prop="name"
          label="姓名"
          width="120">
        </el-table-column>
        <el-table-column
          prop="province"
          label="省份"
          width="120">
        </el-table-column>
        <el-table-column
          prop="city"
          label="市区"
          width="120">
        </el-table-column>
        <el-table-column
          prop="address"
          label="地址"
          width="300">
        </el-table-column>
        <el-table-column
          prop="zip"
          label="邮编"
          width="120">
        </el-table-column>
        <el-table-column
          fixed="right"
          label="操作"
          width="100">
          <template slot-scope="scope">
            <el-button @click="handleClick(scope.row)" type="text" size="small">查看</el-button>
            <el-button type="text" size="small">编辑</el-button>
          </template>
        </el-table-column>
      </el-table>
    </div>

  </div>

</template>

<script>
export default {
  name: "index",
  data() {
    return {
      form: {
        value: '',
        value1: '',
      },
      options: [{
        value: '选项1',
        label: '黄金糕'
      }, {
        value: '选项2',
        label: '双皮奶'
      }, {
        value: '选项3',
        label: '蚵仔煎'
      }, {
        value: '选项4',
        label: '龙须面'
      }, {
        value: '选项5',
        label: '北京烤鸭'
      }],
      tableData: [{
        date: '2016-05-02',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1518 弄',
        zip: 200333
      }, {
        date: '2016-05-04',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1517 弄',
        zip: 200333
      }, {
        date: '2016-05-01',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1519 弄',
        zip: 200333
      }, {
        date: '2016-05-03',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1516 弄',
        zip: 200333
      }]
    }
  },
}
</script>

<style scoped>

</style>
