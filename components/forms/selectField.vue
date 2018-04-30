<template>
	<div>
		<div class="checkbox-block container column flex-grow-1" v-if="config.type === 0">
			<h4 class="checkbox-block__title">{{ config.title }}</h4>
			<div class="checkboxes" v-for="label in config.labels">
				<label for="" class="checkboxes__label" @click="toggleCheck($event)">
					<input type="checkbox" class="checkboxes__input">
					<span>{{ label }}</span>
				</label>
			</div>
		</div>

		<div class="radio-block container column flex-grow-1" v-else-if="config.type === 1">
			<h4 class="radio-block__title">{{ config.title }}</h4>
			<form action="" class="radio-button">
				<div class="radio-button__item" v-for="label in config.labels">
					<label for="" class="radio-button__label" @click="toggleCheck($event)">
						<input type="radio" class="radio-input">
						<span>{{ label }}</span>
					</label>
				</div>
			</form>
		</div>

		<div class="select-block form-field container column" v-if="config.type === 2">
			<label for="" class="select-block__label form-field__label">{{ config.title }}</label>
			<div class="form-field__select">
				<input type="text" class="select-input form-field__input" :value="selectList.selectItem">
				<ul class="select-list" v-bind:class="{ 'select-list___open' : selectList.list}">
					<li class="select-list__item" tabindex="0" :value="label" @click="choseSelect($event)" v-for="label in config.labels"><span>{{ label }}</span></li>
				</ul>
				<i class="material-icons select-icon" @click="toggleSelect()">arrow_drop_down</i>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "selectField",
	props: {
		config: {
			type: Object
		}
	},
	data() {
		return {
			selectList: {
				list: false,
				selectItem: "Escolha"
			},
			toggleCheck(e) {
				let elem = e.target.previousSibling,
						list = e.target.offsetParent.parentNode;
				if(elem.type === "radio") {
					Array.from(list).map(i => {
						i.checked = false;
					});
				}
				return elem.checked ? elem.checked = false : elem.checked = true;
			},
			toggleSelect() {
				return this.selectList.list ? this.selectList.list = false : this.selectList.list = true;
			},
			choseSelect(e) {
				console.dir(e);
				let c = e.target.innerText;
				this.selectList.selectItem = c;
				this.toggleSelect();
			}
		}
	}
}
</script>

<style lang="scss" scoped>

</style>
