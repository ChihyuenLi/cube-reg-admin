  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
<template>
  <!-- <demotable></demotable> -->
  <div>
    <nav>
      <el-button @click="component = 'membertable'">成员数据</el-button>
      <el-button @click="component = 'competitiontable'">比赛数据</el-button>
      <el-button @click="component = 'clubtable'">社团数据</el-button>
    </nav>
  </div>
  <div>
    <keep-alive>
      <component :is="component"></component>
    </keep-alive>
  </div>
</template>



<script>
// import HelloWorld from './components/HelloWorld.vue'
import { ElButton } from 'element-plus';
// import demotable from './tables/demotable.vue';
import clubtable from './tables/clubtable.vue';
import competitiontable from './tables/competitiontable.vue';
import membertable from './tables/membertable.vue';


export default {
  name: 'App',
  components: {
    // HelloWorld,
    // demotable,
    ElButton,
    clubtable,
    competitiontable,
    membertable,
  },
  data() {
    return {
      component: 'membertable', // 默认显示 Component A 组件
    }
  },
}
</script>
