<template>
	<div id="app">
		<FakeBar></FakeBar>
		<router-view></router-view>
	</div>
</template>

<script>
	import FakeBar from './components/Public/FakeBar.vue'
	export default {
		name: 'comfysubs',
		components:{FakeBar}
	}
</script>

<style>
</style>
