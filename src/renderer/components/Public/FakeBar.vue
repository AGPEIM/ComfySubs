<template>
	<div class="fake-title-bar">
	  <div class="handle-bar" v-if="os === 'win32'"> <!-- 如果是windows系统 就加上模拟的操作按钮-->
	    <i class="el-icon-minus" @click="minimizeWindow"></i>
	    <i class="el-icon-close" @click="closeWindow"></i>
	  </div>
	</div>
</template>

<script>
	export default {
	  data () {
	    return {
	      electron: process.versions.electron,
	      name: this.$route.name,
	      node: process.versions.node,
	      path: this.$route.path,
	      platform: require('os').platform(),
	      vue: require('vue/package.json').version
	    }
	  }
	}
</script>

<style scoped>
	.fake-title-bar {
	  -webkit-app-region:drag;
	  height: 22px;
	  width: 100%;
	  text-align: center;
	  color: #4f9589;
	  
	}
	.handle-bar {
	  -webkit-app-region:no-drag
	}
</style>
