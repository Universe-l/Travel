<template>
  <div id="app">
    <keep-alive>
      <router-view/>  <!-- 显示路由所对应的内容 -->
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>

</style>
