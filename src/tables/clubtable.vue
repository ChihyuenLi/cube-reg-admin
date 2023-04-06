<template>
    <div>
        <vxe-table border="inner" :data="tableData">
            <vxe-table-column type="seq" width="60" title="序号"></vxe-table-column>
            <vxe-table-column field="name" title="社团名称"></vxe-table-column>
            <vxe-table-column field="type" title="社团类型"></vxe-table-column>
            <vxe-table-column field="leader" title="社长"></vxe-table-column>
            <vxe-table-column field="memberNum" title="成员数"></vxe-table-column>
        </vxe-table>
    </div>
</template>
    
<script>
import { ref } from 'vue'

export default {
    name: "club-table",
    data() {
        const tableData = ref([
            {
                id: 1,
                name: '音乐社',
                type: '文艺类',
                leader: '张三',
                memberNum: 30
            },
            {
                id: 2,
                name: '篮球社',
                type: '体育类',
                leader: '李四',
                memberNum: 20
            },
            {
                id: 3,
                name: '动漫社',
                type: '文艺类',
                leader: '王五',
                memberNum: 50
            }
        ])
        return {
            tableData
        }
    }
}
</script>