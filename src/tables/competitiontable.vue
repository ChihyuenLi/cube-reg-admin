<template>
    <div>
        <vxe-table border="inner" :data="tableData">
            <vxe-table-column type="seq" width="60" title="序号"></vxe-table-column>
            <vxe-table-column field="name" title="比赛名称"></vxe-table-column>
            <vxe-table-column field="type" title="比赛类型"></vxe-table-column>
            <vxe-table-column field="date" title="比赛时间"></vxe-table-column>
            <vxe-table-column field="winner" title="获胜方"></vxe-table-column>
        </vxe-table>
    </div>
</template>
    
<script>
import { ref } from 'vue'

export default {
    name: "competition-table",
    data() {
        const tableData = ref([
            {
                id: 1,
                name: '篮球比赛',
                type: '体育类',
                date: '2021-10-01',
                winner: 'A队'
            },
            {
                id: 2,
                name: '演讲比赛',
                type: '文艺类',
                date: '2021-11-01',
                winner: 'B队'
            },
            {
                id: 3,
                name: '跳绳比赛',
                type: '体育类',
                date: '2021-12-01',
                winner: 'C队'
            }
        ])
        return {
            tableData
        }
    }
}
</script>
    
    