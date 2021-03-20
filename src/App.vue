<template>
	<div id="app">
		<ul>
			<li :key="item" v-for="item in stuff">
				{{ item }}
			</li>
		</ul>
		<input type="text" v-model="smtext">
		<button @click="appendstuff">ehh</button> 
	</div>
</template>

<script>

export default {
	name: 'App',
	data() {
		return {
			stuff: ["haha", "nub", "die"],
			smtext: null
		}
	},
	methods: {
		appendstuff() {
			if (this.smtext) {
				this.stuff.push(this.smtext)
				this.smtext = null
			} 
		}
	}
}
</script>

<style>
</style>
