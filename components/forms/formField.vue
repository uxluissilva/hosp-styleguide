<!--
TODO:
	- Add input mask for vue
-->

<template>
	<div>
		<div class="form-field container column" v-if="config.style === 'text'">
			<label for="" class="form-field__label">{{ config.label }}</label>
			<input class="form-field__input"
				:type="config.type"
				:name="config.name"
				:placeholder="config.placeholder" />
		</div>
		<div class="form-field container column" v-if="config.style === 'textarea'">
			<label for="" class="form-field__label">{{ config.label }}</label>
			<textarea class="form-field__input"
				:type="config.type"
				:name="config.name"
				:placeholder="config.placeholder" />
		</div>
		<div class="form-field container column" v-else-if="config.style === 'phone'">
			<label for="" class="form-field__label">{{ config.label }}</label>
			<masked-input class="form-field__input"
				:type="config.text"
				:name="config.name"
				:placeholder="config.placeholder"
				:mask="maskType.cellphone"
				:guide="config.guide">
			</masked-input>
		</div>
		<div class="form-field container column" v-else-if="config.style === 'percent'">
			<label for="" class="form-field__label">{{ config.label }}</label>
			<masked-input class="form-field__input"
				:type="config.text"
				:name="config.name"
				:placeholder="config.placeholder"
				:mask="percentMask"
				:guide="config.guide">
			</masked-input>
		</div>
		<div class="form-field container column" v-else-if="config.style === 'email'">
			<label for="" class="form-field__label">{{ config.label }}</label>
			<input class="form-field__input"
				:type="config.text"
				:name="config.name"
				:placeholder="config.placeholder" />
		</div>
		<div class="form-field container column" v-else-if="config.style === 'date'">
			<label for="" class="form-field__label">{{ config.label }}</label>
			<masked-input class="form-field__input"
				:type="config.text"
				:name="config.name"
				:placeholder="config.placeholder"
				:mask="maskType.date"
				:guide="config.guide">
			</masked-input>
		</div>
		<div class="form-field container column" v-else-if="config.style === 'zipcode'">
			<label for="" class="form-field__label">{{ config.label }}</label>
			<masked-input class="form-field__input"
				:type="config.text"
				:name="config.name"
				:placeholder="config.placeholder"
				:mask="maskType.zipcode"
				:guide="config.guide">
			</masked-input>
		</div>
		<div class="form-field container column" v-else-if="config.style === 'cpf'">
			<label for="" class="form-field__label">{{ config.label }}</label>
			<masked-input class="form-field__input"
				:type="config.text"
				:name="config.name"
				:placeholder="config.placeholder"
				:mask="maskType.cpf"
				:guide="config.guide">
			</masked-input>
		</div>
		<div class="form-field container column" v-else-if="config.style === 'rg'">
			<label for="" class="form-field__label">{{ config.label }}</label>
			<masked-input class="form-field__input"
				:type="config.text"
				:name="config.name"
				:placeholder="config.placeholder"
				:mask="maskType.rg"
				:guide="config.guide">
			</masked-input>
		</div>

	</div>
</template>

<script>
import MaskedInput from 'vue-text-mask';
import createNumberMask from 'text-mask-addons/dist/createNumberMask';

export default {
	name: "formField",
	components: {
		MaskedInput
	},
	props: {
		config: {
			type: Object,
			default: {
				style: "text",
				type: "text",
				name: "",
				placeholder: "",
				guide: false,
				label: ""
			}
		}
	},
	data() {
		return {
			maskType: {
				none: "",
				homePhone: ['(', /[1-9]/, /\d/, ')', ' ', /\d/, /\d/, /\d/, /\d/, '-', /\d/, /\d/, /\d/, /\d/],
				cellphone: ['(', /[1-9]/, /\d/, ')', ' ', /\d/, ' ', /\d/, /\d/, /\d/, /\d/, '-', /\d/, /\d/, /\d/, /\d/],
				date: [/\d/, /\d/, '/', /\d/, /\d/, '/', /\d/, /\d/, /\d/, /\d/],
				zipcode: [/\d/, /\d/, /\d/, /\d/, /\d/, '-', /\d/, /\d/, /\d/],
				cpf: [/\d/, /\d/, /\d/, '.', /\d/, /\d/, /\d/, '.', /\d/, /\d/, /\d/, '-', /\d/, /\d/],
				rg: [/\d/, /\d/, '.', /\d/, /\d/, /\d/, '.', /\d/, /\d/, /\d/, '-', /\d/]
			},
			percentMask: createNumberMask({
				prefix: '',
				suffix: ' %',
				allowDecimal: true,
				thousandsSeparatorSymbol: '.',
				decimalSymbol: ','
			})
		}
	}
}
</script>

<style lang="scss" scoped>

</style>
