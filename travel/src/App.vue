<template>
  <div id="app">
    <keep-alive exclude="Detail"><!--只有这个页面不会被本地缓存-->
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
  *{
    font-family: '微软雅黑'
  }
</style>
