<template>
  <div class="demo">
    <Button type="primary" @click="handleClick">Welcome!</Button>
    <Tabs>
        <TabPane label="macOS" icon="logo-apple">标签一的内容</TabPane>
        <TabPane label="Windows" icon="logo-windows">标签二的内容</TabPane>
        <TabPane label="Linux" icon="logo-tux">标签三的内容</TabPane>
    </Tabs>
    <Menu :theme="'dark'" active-name="1-2" :open-names="['1']">
                <Submenu name="1">
                    <template #title>
                        <Icon type="ios-paper" />
                        内容管理
                    </template>
                    <MenuItem name="1-1">文章管理</MenuItem>
                    <MenuItem name="1-2">评论管理</MenuItem>
                    <MenuItem name="1-3">举报管理</MenuItem>
                </Submenu>
                <Submenu name="2">
                    <template #title>
                        <Icon type="ios-people" />
                        用户管理
                    </template>
                    <MenuItem name="2-1">新增用户</MenuItem>
                    <MenuItem name="2-2">活跃用户</MenuItem>
                </Submenu>
                <Submenu name="3">
                    <template #title>
                        <Icon type="ios-stats" />
                        统计分析
                    </template>
                    <MenuGroup title="使用">
                        <MenuItem name="3-1">新增和启动</MenuItem>
                        <MenuItem name="3-2">活跃分析</MenuItem>
                        <MenuItem name="3-3">时段分析</MenuItem>
                    </MenuGroup>
                    <MenuGroup title="留存">
                        <MenuItem name="3-4">用户留存</MenuItem>
                        <MenuItem name="3-5">流失用户</MenuItem>
                    </MenuGroup>
                </Submenu>
            </Menu>
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
}
</style>
