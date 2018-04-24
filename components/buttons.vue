<template>
<div class="size margin">
  <div class="example">
    <titleComponent :config="config.title" />


    <div class="buttons-styleguide container">
      <div class="buttons-block container column flex-grow-1">

        <titleComponent :config="config.subTitle.styles" />

        <div class="buttons-block__item container justify-content-between align-items-center padding-20">
          <div class="container column align-center flex-basis-150">
            <span>Normal</span>
            <span>.button</span>
          </div>
          <div class="button-example container flex-basis-300 justify-content-start align-items-center">
              <buttonStd :config="config.button.normal" />
          </div>
          <div class="code-example container align-center">
            <pre>
              <code class="html">
&lt;buttonStd :config="config.button.normal"&gt;
              </code>
            </pre>
          </div>
        </div>

        <div class="buttons-block__item container justify-content-between align-items-center padding-20">
          <div class="container column align-center flex-basis-150">
            <span>Totem</span>
            <span>&#38;.button-totem</span>
          </div>
          <div class="button-example container flex-basis-300 justify-content-start align-items-center">
            <buttonStd :config="config.button.totem" />
          </div>
          <div class="code-example container align-center">
            <pre>
              <code class="html">
&lt;buttonStd :config="config.button.totem"&gt;
              </code>
            </pre>
          </div>
        </div>

        <div class="buttons-block__item container justify-content-between align-items-center padding-20">
          <div class="container column align-center flex-basis-150">
            <span>Small</span>
            <span>&#38;.button-small</span>
          </div>
          <div class="button-example container flex-basis-300 justify-content-start align-items-center">
            <buttonStd :config="config.button.small" />
          </div>
          <div class="code-example container align-center">
            <pre>
              <code class="html">
&lt;buttonStd :config="config.button.small"&gt;
              </code>
            </pre>
          </div>
        </div>

        <div class="buttons-block__item container justify-content-between align-items-center padding-20">
          <div class="container column align-center flex-basis-150">
            <span>Large</span>
            <span>&#38;.button-large</span>
          </div>
          <div class="button-example container flex-basis-300 justify-content-start align-items-center">
            <buttonStd :config="config.button.large" />
          </div>
          <div class="code-example container align-center">
            <pre>
              <code class="html">
&lt;buttonStd :config="config.button.large"&gt;
              </code>
            </pre>
          </div>
        </div>

        <div class="buttons-block__item container justify-content-between align-items-center padding-20">
          <div class="container column align-center flex-basis-150">
            <span>Stroke</span>
            <span>&#38;.button-stroke</span>
          </div>
          <div class="button-example container flex-basis-300 justify-content-start align-items-center">
            <buttonStd :config="config.button.stroke" />
          </div>
          <div class="code-example container align-center">
            <pre>
              <code class="html">
&lt;buttonStd :config="config.button.stroke"&gt;
              </code>
            </pre>
          </div>
        </div>

        <div class="buttons-block__item container justify-content-between align-items-center padding-20">
          <div class="container column align-center flex-basis-150">
            <span>Flat</span>
            <span>&#38;.button-flat</span>
          </div>
          <div class="button-example container flex-basis-300 justify-content-start align-items-center">
            <buttonStd :config="config.button.flat" />
          </div>
          <div class="code-example container align-center">
            <pre>
              <code class="html">
&lt;buttonStd :config="config.button.flat"&gt;
              </code>
            </pre>
          </div>
        </div>
      </div>
    </div>

    <div class="container column">

      <titleComponent :config="config.subTitle.alert" />
      <div class="container wrap padding-20">
        <buttonStd :config="config.button.normal" :mod="config.button.mods.da"/>
        <pre>
          <code class="html">
&lt;buttonStd :config="config.button.normal" :mod="config.button.mods.da"&gt;
          </code>
        </pre>
      </div>

      <titleComponent :config="config.subTitle.disabled" />
      <div class="container wrap padding-20">
        <buttonStd :config="config.button.normal" :mod="config.button.mods.dis"/>
        <pre>
          <code class="html">
&lt;buttonStd :config="config.button.normal" :mod="config.button.mods.dis"&gt;
          </code>
        </pre>
      </div>

      <titleComponent :config="config.subTitle.icon" />
      <div class="container wrap padding-20">
        <buttonStd :config="config.button.normal" :icon="config.button.ico"/>
        <pre>
          <code class="html">
&lt;buttonStd :config="config.button.normal" :mod="config.button.mods.ico"&gt;
          </code>
        </pre>
      </div>


    </div>

  </div>
</div>
</template>

<script>
import titleComponent from '@/components/titleComponent';
import atomicButton from '@/components/btn/buttonComponent';
import buttonStd from '@/components/btn/button-std';

export default {
  name: 'buttons',
  components: {
    titleComponent,
    atomicButton,
    buttonStd
  },
  data() {
    return {
      config: {
        title: {
          order: 2,
          text: "Botões"
        },
        subTitle: {
          styles: {
            order: 3,
            text: "Tipos de botões"
          },
          alert: {
            order: 3,
            text: "Alerta - danger"
          },
          disabled: {
            order: 3,
            text: "Desabilitado"
          },
          icon: {
            order: 3,
            text: "Ícones"
          }
        },
        button: {
          normal: {
            style: "",
            text: "Button"
          },
          totem: {
            style: "totem",
            text: "Atendimento"
          },
          small: {
            style: "sm",
            text: "Outros"
          },
          large: {
            style: "lg",
            text: "Participar"
          },
          stroke: {
            style: "stk",
            text: "Relatório"
          },
          flat: {
            style: "flat",
            text: "Login"
          },
          mods: {
            dis: "disabled",
            da: "alert",
          },
          ico: {
            class: "icon",
            name: "settings"
          }
        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.buttons-styleguide {
  width: 100%;

  .buttons-block {
    .buttons-block__item {
      width: 100%;

      .button-example {

      }
    }
  }
}

.ex-btn {
    padding-bottom: 100px;
}
.esp {
    margin-bottom: 10px;
}
table {
    border-collapse: collapse;
    width: 100%;
}

td,
th {
    border: 1px solid #ccc;
    text-align: left;
    padding: 8px;
}
tr:nth-child(even) {
    background-color: #ddd;
}
.table {
    width: 1200px;
    max-width: 100%;
    overflow-x: scroll;
}
table,
td,
th,
tr {}
</style>
