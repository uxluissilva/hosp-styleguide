<template>
	<div class="">
		<div class="button" v-if="!config.style && !config.mod && !config.icon">
			<a href="#!">{{ config.text }}</a>
		</div>
		<div class="button" :class="'button-' + config.style" v-else-if="config.style && !config.mod && !config.icon">
			<a href="#!">{{ config.text }}</a>
		</div>
		<div class="button" :class="mod" v-else-if="!config.style && config.mod && !config.icon">
			<a href="#!">{{ config.text }}</a>
		</div>
		<div class="button" :class="'button-' + config.style + ' ' + config.mod" v-else-if="config.style && config.mod && !config.icon">
			<a href="#!">{{ config.text }}</a>
		</div>
		<div class="button container align-items-center" :class="'button-' + config.style + ' ' + config.mod + ' button-icon'" v-else-if="config.icon">
			<i class="material-icons">{{ config.icon }}</i> <a href="#!">{{ config.text }}</a>
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

<style lang="scss" >
@import '~assets/css/styleguide/buttons.scss';
</style>
