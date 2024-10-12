<template>
  <div class="demo">
    <Button type="primary" @click="handleClick">Welcome!</Button>
    <Tabs>
        <TabPane label="macOS" icon="logo-apple">标签一的内容</TabPane>
        <TabPane label="Windows" icon="logo-windows">标签二的内容</TabPane>
        <TabPane label="Linux" icon="logo-tux">标签三的内容</TabPane>
    </Tabs>
  </div> 
</template>

<script>
export default {
  name: 'HomeView',
  components: {
  },
  setup() {
  },
  methods: {
    handleClick() {
      this.$Message.info('Welcome to View UI Plus Demo!')
    }
  }
}
</script>

<style lang="less" scoped>
.demo{
  color: lightcoral;
  font-size: @font-size;
  text-align: center;
  margin: 300px 0 0 0;
}
</style>
