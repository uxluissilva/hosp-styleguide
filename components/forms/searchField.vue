<template lang="html">
  <div class="">
    <div class="form-field container column">
      <label for="" class="form-field__label">{{ config.label }}</label>
      <div class="container align-items-center search-block">
        <i class="material-icons">search</i>
        <input type="text" id="search-field" class="form-field__input margin-right-20" :placeholder="config.placeholder">
        <buttonStd :config="config.button" />
      </div>
    </div>
  </div>
</template>

<script>

import buttonStd from '@/components/btn/button-std';

export default {
  name: "searchField",
  components: {
    buttonStd
  },
  props: {
    config: {
      type: Object,
      default: {
        style: "search",
        placeholder: "",
        label: "Search",
        button: {
          style: "",
          text: "Search"
        }
      }
    }
  },
  data() {
    return {

    }
  }
}
</script>

<style lang="css">
</style>
