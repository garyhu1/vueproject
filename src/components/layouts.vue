<template>
	<section class="container" v-bind:class="{'menu-open':menuOpen}"><!--最外层容器-->
		<section class="menu">
			<!--左边的容器-->
			<!--<menu :todoList="todoList" :id="todoId" @go-list="goList"></menu>-->
			<menus></menus>
		</section>
		<section class="content-container"><!--右边的容器-->
           <todo></todo>
        </section>
		<!--<div class="content-overlay" @click="$store.dispatch('updateMenu')"></div>-->
		<!--<div class="content-container">--><!--右边的容器-->
			<!--<router-view></router-view>-->
		<!--</div>-->
	</section>
</template>

<script>
	import menus from './menus';  // 导入刚才我们创建的 menus组件
	import todo from './todo';
	export default {
		components : {
			menus ,// 注册menus组件，让其可以在template调用
			todo
		}
	};
</script>

<style lang="less">/*使用.less文件*/
	@import '../common/style/layouts.less';
</style>