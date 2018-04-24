<template>
	<div class="">
		<div class="button" v-if="!config.style && !mod && !icon">
			<span>{{ config.text }}</span>
		</div>
		<div class="button" :class="'button-' + config.style" v-else-if="config.style && !mod && !icon">
			<span>{{ config.text }}</span>
		</div>
		<div class="button" :class="mod" v-else-if="!config.style && mod && !icon">
			<span>{{ config.text }}</span>
		</div>
		<div class="button" :class="'button-' + config.style + ' ' + mod" v-else-if="config.style && mod && !icon">
			<span>{{ config.text }}</span>
		</div>
		<div class="button container align-items-center" :class="'button-' + config.style + ' ' + mod + ' button-' + icon.class" v-else-if="icon">
			<i class="material-icons">{{ icon.name }}</i> <span>{{ config.text }}</span>
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
		},
		mod: {
			type: String
		},
		icon: {
			type: Object
		}
	},
	data() {
		return {}
	}
}
</script>

<style lang="scss" >
@import '~assets/css/base/variables.scss';
@import '~assets/css/base/mixins.scss';
@import '~assets/css/base/material-shadows.scss';

.button {
  height: auto;
  width: fit-content;
  padding: 12px 30px;
  color: $color-white;
  background: $color-primary;
  font-size: $font-size-lg;
  text-align: center;
  border-radius: 8px;
  box-sizing: border-box;
  user-select: none;
  cursor: pointer;

  @include toggle-transition($sec: .18s);
  @include z-depth(4);

  &.button-icon {

    span, i {
      margin: 0 -5px;
    }

    i {
      vertical-align: middle;
      margin-right: 17px;
    }
  }

  &.button-totem {
    padding: 50px 60px;
    font-size: $font-size-xx;
    @include z-depth(8);

    i {
      font-size: $font-size-xx;
    }

    &:hover {
      @include z-depth(16);
    }
    &:active {
      @include z-depth(4);
      @include toggle-transition($sec: .08s, $form: ease-in);
    }
  }

  &.button-sm {
    padding: 8px 25px;
    font-size: $font-size-sm;
  }

  &.button-lg {
    padding: 20px 40px;
  }

  &.button-stk {
    background: transparent;
    border: 1px solid $color-primary;
    box-shadow: none;
    color: $color-primary;

    &:hover {
      color: $color-white;
      background: $color-primary;
      box-shadow: none;
    }

    &:active {
      box-shadow: none;
    }

    &.alert {
      background: transparent;
      border-color: $color-danger;
      color: $color-danger;

      &:hover {
        color: $color-white;
        background: $color-danger;
        box-shadow: none;
      }
    }
  }

  &.button-flat {
    background: transparent;
    color: $color-primary;
    box-shadow: none;

    &:hover {
      background: none;
      box-shadow: none;
    }

    &:active {
      box-shadow: none;
    }

    &.alert {
      background: transparent;
      color: $color-danger;
    }
  }

  &:hover {
    filter: opacity(.9);
    @include z-depth(8);
  }

  &:active {
    filter: opacity(1);
    @include z-depth(2);
    @include toggle-transition($sec: .05s, $form: ease-in);
  }

  &.disabled {
    opacity: 0.5;
    box-shadow: none;
    cursor: not-allowed;

    &:hover,
    &:active,
    &:focus {
      box-shadow: none;
      filter: none;
    }
  }

  &.alert {
    background: $color-danger;
  }
}
</style>
