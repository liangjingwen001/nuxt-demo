<template>
  <div class="container">
    <div>我是首页</div>
    <div v-for="item in detail">{{item.id}}-{{item.title}}</div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue';
import axios from 'axios';

export default {
    Components: {
        Logo
    },
    data() {
        return {
            dataList: ''
        }
    },
    // 请求数据
    async asyncData() {
        // return axios.get('http://jsonplaceholder.typicode.com/posts').then((res) => {
        //     console.log(res)
        //     return {
        //         detail: res.data
        //     }
        // })
        
        const res = await axios.get('http://jsonplaceholder.typicode.com/posts')
        return {
            detail: res.data
        }
    },
    created() {
        console.log(this.dataList)
    }
}
</script>

<style>

</style>


