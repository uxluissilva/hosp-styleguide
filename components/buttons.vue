<template>
<div class="size margin">
  <div class="example">
    <titleComponent :config="config.title" />

    <div class="buttons-styleguide container column">
      <div class="buttons-type">
        <titleComponent :config="config.subTitle.type" />
        <div class="container column padding-20">
          <p>O componente de botão utiliza o seguinte objeto.</p>
          <pre>
            <code class="javascript">
config: {
  style: String, // estilo do botão, default = "normal"
  text: String, // texto do botão
  mod: String, // modificador, ex: "alert"
  icon: String // nome do ícone material-icons
}
            </code>
          </pre>
        </div>
      </div>

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
      <div class="container column padding-left-20">
        <span>&#38;.alert</span>
      </div>

      <div class="container wrap padding-20">
        <buttonStd :config="config.button.normalAlert"/>
        <pre>
          <code class="html">
&lt;buttonStd :config="config.button.normalAlert"&gt;
          </code>
        </pre>
      </div>

      <titleComponent :config="config.subTitle.disabled" />
      <div class="container column padding-left-20">
        <span>&#38;.disabled</span>
      </div>

      <div class="container wrap padding-20">
        <buttonStd :config="config.button.normalDisabled"/>
        <pre>
          <code class="html">
&lt;buttonStd :config="config.button.normalDisabled"&gt;
          </code>
        </pre>
      </div>

      <titleComponent :config="config.subTitle.icon" />
      <div class="container column padding-left-20">
        <span>&#38;.button-icon</span>
      </div>

      <div class="container wrap padding-20">
        <buttonStd :config="config.button.normalIcon"/>
        <pre>
          <code class="html">
&lt;buttonStd :config="config.button.normalIcon"&gt;
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
          type: {
            order: 3,
            text: "Componente - Object type"
          },
          styles: {
            order: 3,
            text: "Tipos de botões"
          },
          alert: {
            order: 4,
            text: "Alerta - danger"
          },
          disabled: {
            order: 4,
            text: "Desabilitado"
          },
          icon: {
            order: 4,
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
          normalAlert: {
            style: "normal",
            text: "Button",
            mod: "alert"
          },
          normalDisabled: {
            style: "normal",
            text: "Button",
            mod: "disabled"
          },
          normalIcon: {
            style: "normal",
            text: "Button",
            icon: "settings"
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
