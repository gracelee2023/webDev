<!-- Element组件包括3个部分：
1.template 用来定义HTML页面模版; 2. script 用来定义vue中的数据模型以及方法，也就是js文件； 3. style 用来定义css样式代码-->


<template>
    <div>
        <!-- Button按钮 -->
        <el-row>
        <el-button>默认按钮</el-button>
        <el-button type="primary">主要按钮</el-button>
        <el-button type="success">成功按钮</el-button>
        <el-button type="info">信息按钮</el-button>
        <el-button type="warning">警告按钮</el-button>
        <el-button type="danger">危险按钮</el-button>
        </el-row>

        <!-- 换行标签 -->
        <br>

        <!-- Table -->
        <!-- data绑定了tableData这个数据；
        border：带边框
        prop： 这一列展示的是这个对象的什么属性
        label： 表头的名称 -->


        <el-table
        :data="tableData"

        border
        style="width: 100%">
        <el-table-column
        prop="date"
        label="日期"
        width="180">
        </el-table-column>
        <el-table-column
        prop="name"
        label="姓名"
        width="180">
        </el-table-column>
        <el-table-column
        prop="address"
        label="地址">
        </el-table-column>
        </el-table>

        <!-- Pagination分页 -->
        <!-- sizes: XX条/页
        jumper：前往X页 -->
        <el-pagination background layout="total, sizes, prev, pager, next, jumper"
        :total="1000">
        </el-pagination>

        

    </div>
</template>

<script>
export default {
    // Table内容
    data(){
        return {
            tableData: [{
          date: '2016-05-02',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1518 弄'
        }, {
          date: '2016-05-04',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1517 弄'
        }, {
          date: '2016-05-01',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1519 弄'
        }, {
          date: '2016-05-03',
          name: '王小虎',
          address: '上海市普陀区金沙江路 1516 弄'
        }]
        }
    }
    
}
</script>

<style>

</style>