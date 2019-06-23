<template>
  <div class="content" @click="a">  
    {{testdata}}
    <el-button type="primary" round>主要按钮</el-button>
  </div>
</template>

<script>
import { CLIENT_RENEG_LIMIT } from 'tls';

  export default {
    name:'test', 
    props:[''],
    data () {
      return {
          testdata:'陈艾伦是个傻小子'
      };
    },
    components: {},
    computed: {},
    beforeCreate(){
        console.log('创建前')
    },
    created(){
        console.log('创建后')
    },
    beforeMount() {
        console.log('挂载前')
    },
    mounted() {
        console.log('挂载后')
        this.testdata = this.testdata +'不仅傻还笨'
    },
    beforeDestroy(){
        console.log('销毁前');
    },
    destroyed(){
        console.log('销毁后')
    },
    methods: {
       a(){
        console.log('其实你还是很聪明的')
       },
       b(){}
    },
    watch: {}
  }
</script>

<style lang="scss" scoped>
    .content{
        background-color: red;
    }
</style>
