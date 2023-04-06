<template>
    <div>
        <vxe-table border="inner" :data="tableData">
            <vxe-table-column type="seq" width="60" title="序号"></vxe-table-column>
            <vxe-table-column field="name" title="姓名"></vxe-table-column>
            <vxe-table-column field="gender" title="性别"></vxe-table-column>
            <vxe-table-column field="age" title="年龄"></vxe-table-column>
            <vxe-table-column field="club" title="所属社团"></vxe-table-column>
        </vxe-table>
    </div>
</template>
    
<script>
import { ref } from 'vue'

export default {
    name: "member-table",
    data() {
        const tableData = ref([
            {
                id: 1,
                name: '张三',
                gender: '男',
                age: 18,
                club: '音乐社'
            },
            {
                id: 2,
                name: '李四',
                gender: '女',
                age: 19,
                club: '篮球社'
            },
            {
                id: 3,
                name: '王五',
                gender: '男',
                age: 20,
                club: '动漫社'
            }
        ])
        return {
            tableData
        }
    }
}
</script>