<template>
	<div>
		<div v-if="selection == 'Contact'">
			<h3> Find me at: </h3>
			<p> NYC </p>
		</div>
		<div v-else-if="selection == 'Work'">
			<h2> Portfolio </h2>
			<a href="https://www.github.com/pmocal"> My Github </a>
			<h2> Resume </h2>
			<a href="./ParthivMohanResumeWithoutAddress.pdf" target="_blank">Link</a>
			<h2> LinkedIn </h2>
			<a href="https://www.linkedin.com/in/parthivmohan">Link</a>
		</div>
		<div v-else-if="selection == 'Home'">
			<h1> Welcome to Parthiv Mohan's website </h1>
		</div>
	</div>
</template>

<script>

	export default {
		name: "Pages",
		props: ['selection']
	}

</script>

<style scoped>
	
	h1 {
		font-weight: bolder;
	}

	h2 {
		font-weight: bold
	}

	p {
		color: orange;
	}

	div div * {
		text-align: center;
		margin: 5%;
	}

</style>