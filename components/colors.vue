<template>
<div class="size margin">

  <div class="example">
    <titleComponent :config="configColors" />
    <div class="container column">

      <titleComponent :config="configColors.primary" />

      <div class="container wrap">
        <div class="box-colors text-center container column align-items-center" v-for="x in colors.primary">
          <div class="box" :style="{ background: x.hex }"></div>
          <div class="text">
            <strong>{{x.name}}</strong>
            <p><small>{{x.hex}}</small></p>
          </div>
        </div>
      </div>

      <titleComponent :config="configColors.secondary" />

      <div class="container wrap">
        <div class="box-colors text-center container column align-items-center" v-for="x in colors.secondary">
          <div class="box" :style="{ background: x.hex }"></div>
          <div class="text">
            <strong>{{x.name}}</strong>
            <p><small>{{x.hex}}</small></p>
          </div>
        </div>
      </div>

      <titleComponent :config="configColors.comp" />

      <div class="container wrap">
        <div class="box-colors text-center container column align-items-center" v-for="x in colors.complement">
          <div class="box" :style="{ background: x.hex }"></div>
          <div class="text">
            <strong>{{x.name}}</strong>
            <p><small>{{x.hex}}</small></p>
          </div>
        </div>
      </div>

      <titleComponent :config="configColors.bw" />

      <div class="container wrap">
        <div class="box-colors text-center container column align-items-center" v-for="x in colors.blackWhite">
          <div class="box" :style="{ background: x.hex }"></div>
          <div class="text">
            <strong>{{x.name}}</strong>
            <p><small>{{x.hex}}</small></p>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="example">
    <titleComponent :config="configGrad" />

    <div class="container column wrap">
      <!-- background: linear-gradient(10deg, #333, #222); -->
      <div v-for="x in gradients" class="flex-grow-1">
        <div class="box-gradient text-center container justify-content-center align-items-center" :style="{background: 'linear-gradient(to right,' + x.color + ',' + x.color2 + ')'}">
          <div class="text container column">
            <strong>{{x.name}}</strong>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="example">
    <titleComponent :config="configShadows" />

    <div class="container wrap">
      <div class="box-shadow text-center container justify-content-center align-items-center" v-for="x in shadows" :class="x.name">
        <div class="text container column">
          <strong>{{x.name}}</strong>
          <!-- <small style="font-size: 10px">box-shadow: 0 0 {{x.size}}px {{x.smooth}}px rgba(0,0,0,.1)</small> -->
        </div>
      </div>
    </div>
  </div>

</div>
</template>

<script>
import titleComponent from '@/components/titleComponent'

export default {
  name: 'colors',
  components: {
    titleComponent
  },
  name: 'colors',
  data() {
    return {
      configColors: {
        order: 2,
        text: "Cores",
        primary: {
          order: 3,
          text: "Cores Primárias"
        },
        secondary: {
          order: 3,
          text: "Cores Secundárias"
        },
        comp: {
          order: 3,
          text: "Cores Complementares"
        },
        bw: {
          order: 3,
          text: "Black & White"
        }
      },
      configGrad: {
        order: 2,
        text: "Gradientes"
      },
      configShadows: {
        order: 2,
        text: "Shadows"
      },
      colors: {
        primary: [
          {
          name: 'Primary',
          hex: '#3f51b5'
          },
          {
            name: 'Primary light',
            hex: '#757de8'
          },
          {
            name: 'Primary dark',
            hex: '#002984'
          }
        ],
        secondary: [
          {
          name: 'Secondary',
          hex: '#b0bec5'
          },
          {
            name: 'Secondary light',
            hex: '#e2f1f8'
          },
          {
            name: 'Secondary dark',
            hex: '#808e95'
          }
        ],
        complement: [
          {
          name: 'Complete',
          hex: '#219653'
          },
          {
            name: 'Danger',
            hex: '#eb5757'
          },
          {
            name: 'Warning',
            hex: '#f2c94c'
          },
          {
            name: 'Alert',
            hex: '#f2994a'
          }
        ],
        blackWhite: [
          {
            name: 'Black',
            hex: '#333333'
          },
          {
            name: 'Dark',
            hex: '#4f4f4f'
          },
          {
            name: 'Grey',
            hex: '#e1e2e1'
          },
          {
            name: 'White',
            hex: '#f2f2f2'
          },
          {
            name: 'White-light',
            hex: '#ffffff'
          }
        ]
      },
      shadows: [{
          name: 'shadow-2dp'
        },
        {
          name: 'shadow-3dp'
        },
        {
          name: 'shadow-4dp'
        },
        {
          name: 'shadow-6dp'
        },
        {
          name: 'shadow-8dp'
        },
        {
          name: 'shadow-16dp'
        },
        {
          name: 'shadow-24dp'
        }
      ],
      gradients: [{
          name: 'Primary',
          color: '#757de8',
          color2: '#002984'
        },
        {
          name: 'Dark',
          color: '#808e95',
          color2: '#000000'
        },
        {
          name: 'Light',
          color: '#e2f1f8',
          color2: '#808e95'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.box-colors {
    flex-basis: 130px;
    box-shadow: 0 0 10px 0 rgba(0,0,0,.1);
    box-sizing: border-box;
    padding-top: 0 !important;
    .box {
        width: 130px;
        height: 100px;
    }
    .text {
        padding-top: 10px;
    }
    &:hover {
        box-shadow: 0 10px 10px 0 rgba(0,0,0,.1);
        transform: translateY(-10px);
    }
}

.box-shadow {
    flex-basis: 300px;
    flex-grow: 1;
    height: 200px;
    &:hover {
        box-shadow: 0 10px 10px 0 rgba(0,0,0,.1);
        transform: translateY(-10px);
    }
}

.box-gradient {
    flex-basis: 300px;
    flex-grow: 1;
    color: #fff;
    box-shadow: 0 0 10px 0 rgba(0,0,0,.1);
    &:hover {
        box-shadow: 0 10px 10px 0 rgba(0,0,0,.1);
        transform: translateY(-10px);
    }
}

.box-colors,
.box-gradient,
.box-shadow {
    border-radius: 10px;
    overflow: hidden;
    cursor: pointer;
    transition: 0.3s;
    padding: 20px;
    box-sizing: border-box;
    margin: 20px;
    min-height: 130px;
}
</style>
