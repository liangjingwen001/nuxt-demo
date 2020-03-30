<template>
  <div class="container">
    <div>动态路由页面,路由id：{{$route.params.id}}</div>
  </div>
</template>

<script>
export default {
    validata({data}) {
        return false
    }
}
</script>