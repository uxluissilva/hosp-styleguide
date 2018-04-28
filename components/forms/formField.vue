<!--
TODO:
	- Add input mask for vue
-->

<template>
	<div>
		<div class="form-field container column" v-if="config.style === 0 && !config.placeholder">
			<label for="" class="form-field__label">{{ config.label }}</label>
			<input type="text" class="form-field__input">
		</div>
		<div class="form-field container column" v-else-if="config.style === 0 && config.placeholder">
			<label for="" class="form-field__label">{{ config.label }}</label>
			<input type="text" class="form-field__input" :placeholder="config.placeholder">
		</div>
	</div>
</template>

<script>
export default {
	name: "formField",
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
