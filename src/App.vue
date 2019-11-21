<template>
	<div id="app">
		<div id="menu">
			<ul>
				<li v-on:click="selectTab('Home')"><a>Home</a></li>
				<li v-on:click="selectTab('Work')"><a>Work</a></li>
				<li v-on:click="selectTab('Contact')"><a>Contact</a></li>
			</ul>
		</div>
		<pages id="content" :selection="selection"/>
	</div>
</template>

<script>
	import Pages from './components/Pages.vue'

	export default {
		name: 'app',
		data() {
			return {
				selection: 'Home',
			}
		},
		components: {
			Pages
		},
		methods: {
			selectTab(string) {
				this.selection = string;
			}
		}
	}
</script>

<style scoped>
  
	#app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		color: #2c3e50;
		min-height: 100%;
		display: flex;
		flex-wrap: wrap;
	}
	
	#menu {
		width: 100%;
	}
  
	ul {
		justify-content: center;
		display: flex;
	}

	li {
		margin: 5%;
		justify-content: space-between;
	}

	#content {
		width: 100%;
	}

</style>
