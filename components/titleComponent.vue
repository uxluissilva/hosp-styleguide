<template>
<div>

  <div class="title padding-left-20" v-if="config.order === 2">
    <h2>{{ config.text }}</h2>
  </div>
  <div class="sub-title padding-left-20" v-else-if="config.order === 3">
    <h3>{{ config.text }}</h3>
  </div>
  <div class="sub-title padding-left-20" v-else-if="config.order === 4">
    <h4>{{ config.text }}</h4>
  </div>
  <div class="sub-title padding-left-20" v-else-if="config.order === 5">
    <h5>{{ config.text }}</h5>
  </div>
  <div class="sub-title padding-left-20" v-else-if="config.order === 6">
    <h6>{{ config.text }}</h6>
  </div>


</div>
</template>

<script>
export default {
  name: 'titleComponent',
  data() {
    return {
    }
  },
  props: {
    config: {
      type: Object
    }
  }
}
</script>

<style lang="scss" scoped>
.title {
    padding-bottom: 50px;
    h2 {
        position: relative;
        &::after {
            content: '';
            display: block;
            position: absolute;
            background: #2BDBFF;
            width: 120px;
            height: 10px;
            left: 0;
            bottom: -15px;
        }
    }
}
</style>
