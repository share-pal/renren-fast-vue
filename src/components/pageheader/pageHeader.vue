<template>
  <div style="display: flex;font-size: 20px;font-weight: 500;cursor:pointer;">
    <div style="display: flex;" @click="goback()">
      <div><i class="el-icon-back"></i></div>
      <div style="margin: 0 20px">返回</div>
    </div>
    <div>{{ name }}</div>
  </div>
</template>

<script>
export default {
  name: "pageHeader",
  props: ['name'],
  methods: {
    goback() {
      this.$emit('goBack')
    }
  }
}
</script>

<style scoped>

</style>
