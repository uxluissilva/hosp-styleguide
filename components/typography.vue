<template>
<div class="size margin">

  <div class="example">
    <titleComponent :config="config.cal" />

    <div class="container-font-example container column">
      <div class="font-example container wrap">
        <div class="flex-basis-100 flex-grow-1">
          <ul class="list-none">
            <li><strong>Font family:</strong> Arial</li>
            <li><strong>Styles:</strong></li>
          </ul>
        </div>
        <div class="flex-basis-100 flex-grow-1">
          <ul class="list-none">
            <li>
              <p class="font-regular">Regular</p>
            </li>
            <!-- <li>
              <p class="font-light">Light</p>
            </li> -->
            <li>
              <p class="font-italic">Italic</p>
            </li>
            <li>
              <p class="font-semibold">Semibold</p>
            </li>
            <li>
              <p class="font-bold">Bold</p>
            </li>
          </ul>
        </div>
        <div class="flex-basis-400 flex-grow-3 container wrap justify-content-center align-items-center">
          <div class="flex-basis-200 flex-grow-1">
            <h1 class="font-regular">Aa</h1>
            <h5 class="font-regular">Arial Regular</h5>
          </div>
          <div class="flex-basis-200 flex-grow-1">
            <h1 class="font-italic">Aa</h1>
            <h5 class="font-italic">Arial Italic</h5>
          </div>
          <div class="flex-basis-200 flex-grow-1">
            <h1 class="font-bold">Aa</h1>
            <h5 class="font-bold">Arial Bold</h5>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="example">
    <titleComponent :config="config.typ" />

    <div class="container-font-example container column">
      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <ul class="list-none">
            <li>
              <h4>Heading 1</h4></li>
            <li><strong>Font family:</strong> {{text.font.primary}}</li>
            <li><strong>Font size:</strong> 54px</li>
          </ul>
        </div>
        <div class="flex-basis-400 flex-grow-2">
          <h1>Almost before we knew it, we had left the ground.</h1>
        </div>
      </div>
      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <ul class="list-none">
            <li>
              <h4>Heading 2</h4></li>
            <li><strong>Font family:</strong> {{text.font.primary}}</li>
            <li><strong>Font size:</strong> 44px</li>
          </ul>
        </div>
        <div class="flex-basis-400 flex-grow-2">
          <h2>Almost before we knew it, we had left the ground.</h2>
        </div>
      </div>
      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <ul class="list-none">
            <li>
              <h4>Heading 3</h4></li>
            <li><strong>Font family:</strong> {{text.font.primary}}</li>
            <li><strong>Font size:</strong> 36px</li>
          </ul>
        </div>
        <div class="flex-basis-400 flex-grow-2">
          <h3>Almost before we knew it, we had left the ground.</h3>
        </div>
      </div>
      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <ul class="list-none">
            <li>
              <h4>Heading 4</h4></li>
            <li><strong>Font family:</strong> {{text.font.primary}}</li>
            <li><strong>Font size:</strong> 24px</li>
          </ul>
        </div>
        <div class="flex-basis-400 flex-grow-2">
          <h4>Almost before we knew it, we had left the ground.</h4>
        </div>
      </div>
      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <ul class="list-none">
            <li>
              <h4>Heading 5</h4></li>
            <li><strong>Font family:</strong> {{text.font.primary}}</li>
            <li><strong>Font size:</strong> 18px</li>
          </ul>
        </div>
        <div class="flex-basis-400 flex-grow-2">
          <h5>Almost before we knew it, we had left the ground.</h5>
        </div>
      </div>
      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <ul class="list-none">
            <li>
              <h4>Heading 6</h4></li>
            <li><strong>Font family:</strong> {{text.font.primary}}</li>
            <li><strong>Font size:</strong> 16px</li>
          </ul>
        </div>
        <div class="flex-basis-400 flex-grow-2">
          <h6>Almost before we knew it, we had left the ground.</h6>
        </div>
      </div>
    </div>
  </div>

  <div class="example">
    <titleComponent :config="config.p" />

    <div class="container-font-example container column">
      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <h4>b.</h4>
        </div>
        <div class="flex-basis-400 flex-grow-2 font-size">
          <b>Almost before we knew it, we had left the ground.</b>
        </div>
      </div>

      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <h4>p.</h4>
        </div>
        <div class="flex-basis-400 flex-grow-2 font-size">
          <p>Almost before we knew it, we had left the ground.</p>
        </div>
      </div>

      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <h4>small.</h4>
        </div>
        <div class="flex-basis-400 flex-grow-2 font-size">
          <small>Almost before we knew it, we had left the ground.</small>
        </div>
      </div>

      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <h4>span.</h4>
        </div>
        <div class="flex-basis-400 flex-grow-2 font-size">
          <span>Almost before we knew it, we had left the ground.</span>
        </div>
      </div>

      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <h4>i.</h4>
        </div>
        <div class="flex-basis-400 flex-grow-2 font-size">
          <i>Almost before we knew it, we had left the ground.</i>
        </div>
      </div>

      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <h4>u.</h4>
        </div>
        <div class="flex-basis-400 flex-grow-2 font-size">
          <u>Almost before we knew it, we had left the ground.</u>
        </div>
      </div>

      <div class="font-example container">
        <div class="flex-basis-100 flex-grow-1">
          <h4>strike.</h4>
        </div>
        <div class="flex-basis-400 flex-grow-2">
          <strike>Almost before we knew it, we had left the ground.</strike>
        </div>
      </div>
    </div>
  </div>

  <div class="">
    <titleComponent :config="config.font" />

    <div class="container-font-example container column">
      <div class="font-example container wrap">
        <div class="flex-basis-400 flex-grow-3 container wrap justify-content-center align-items-center">
          <div class="box-font flex-basis-200 flex-grow-1 text-left">
            <h1>Aa</h1>
            <h5>Text-left</h5>
          </div>
          <div class="box-font flex-basis-200 flex-grow-1 text-center">
            <h1>Aa</h1>
            <h5>Text-center</h5>
          </div>
          <div class="box-font flex-basis-200 flex-grow-1 text-right">
            <h1>Aa</h1>
            <h5>Text-right</h5>
          </div>
        </div>
      </div>
    </div>
  </div>

</div>
</template>

<script>
import titleComponent from '@/components/titleComponent'

export default {
  name: 'topo',
  components: {
    titleComponent
  },
  data() {
    return {
      config: {
        cal: {
          order: 2,
          text: "Caligrafia"
        },
        typ: {
          order: 2,
          text: "Tipografia"
        },
        p: {
          order: 2,
          text: "Parágrafo"
        },
        font: {
          order: 2,
          text: "Alinhamento"
        }
      },
      text: {
        font: {
          primary: "Arial",
          secondary: "sans-serif"
        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.container-font-example {
    padding-top: 20px;
    .font-example {
        padding: 20px;
        box-sizing: border-box;
        margin-bottom: 20px;
    }
}

.box-font {
    border: 1px solid rgba(0,0,0,.1);
    border-radius: 4px;
    padding: 20px;
    box-sizing: border-box;
    margin: 5px;
}
</style>
