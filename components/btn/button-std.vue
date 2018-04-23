<template>
	<div>
		<!-- <div class="button" v-if="">
		
		</div>
		<div class="button" :class="'button-' + config.style" v-else-if="">
			
		</div> -->
		<div class="button" :class="'button-' + config.style + config.mod" v-else-if="">
			
		</div>
	</div>
</template>

<script>
export default {
	components: {
	},
	props: {
		config: {
			type: Object
		}
	},
	data() {
		return {}
	}
}
</script>

<style lang="scss" scoped>
	
</style>