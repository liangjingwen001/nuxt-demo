<template>
  <div class="container">
    <div>我是用户列表页面</div>
    <!-- 嵌套路由 -->
    <nuxt-link to="/user/">子页面</nuxt-link>
    <nuxt-link to="/user/detail">详情页面</nuxt-link>
    <nuxt />
    <br>
    <input type="text" v-model="id">
    <button @click="toId">动态路由</button>
  </div>
</template>

<script>
export default {
    data() {
        return {
            id: 0
        }
    },
    methods: {
        toId() {
            this.$router.push('/user/' + this.id)
        }
    }
}
</script>