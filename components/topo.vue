<template>
<div>

  <header>
    <div class="header container column align-items-center justify-content-center">
      <div class="block text-center">
        <img src="~/static/logo-benner.svg" class="logo" alt="">
        <p>
          <blockquote>Styleguide do produto <strong>Hospitalar</strong> para maior consistência no design de interfaces do sistema.</blockquote>
        </p>
      </div>
    </div>
  </header>

</div>
</template>

<script>
export default {
  name: 'topo',
  data() {
    return {

    }
  }
}
</script>

<style lang="scss" scoped>
.header {
    min-height: 100vh;
    width: 100%;
    .block {
        width: 600px;
        max-width: 90%;
        img {
            width: 400px;
            max-width: 90%;
            padding-bottom: 20px;
        }
        blockquote {
            font-size: 20px;
            span {
                opacity: 0.5;
            }
        }
    }
}
</style>
