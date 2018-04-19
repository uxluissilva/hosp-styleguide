<template>
<div class="size margin">

  <div class="example">
    <titleComponent>
      <span slot="title">Colors</span>
    </titleComponent>
    <div class="container column">
      
      <h3 class="sub-title">Cores primárias</h3>
      <div class="container wrap">
        <div class="box-colors text-center container column align-items-center" v-for="x in colors.primary">
          <div class="box" :style="{ background: x.hex }"></div>
          <div class="text">
            <strong>{{x.name}}</strong>
            <p><small>{{x.hex}}</small></p>
          </div>
        </div>
      </div>

      <h3 class="sub-title">Cores secundárias</h3>
      <div class="container wrap">
        <div class="box-colors text-center container column align-items-center" v-for="x in colors.secondary">
          <div class="box" :style="{ background: x.hex }"></div>
          <div class="text">
            <strong>{{x.name}}</strong>
            <p><small>{{x.hex}}</small></p>
          </div>
        </div>
      </div>

      <h3 class="sub-title">Cores complementares</h3>
      <div class="container wrap">  
        <div class="box-colors text-center container column align-items-center" v-for="x in colors.complement">
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
    <titleComponent>
      <span slot="title">Gradients</span>
    </titleComponent>
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
    <titleComponent>
      <span slot="title">Shadows</span>
    </titleComponent>
    <div class="container wrap">
      <div class="box-shadow text-center container justify-content-center align-items-center" v-for="x in shadows" :style="{ boxShadow: '0 ' + '0 ' + x.size + 'px ' + x.smooth + 'px ' +  'rgba(0,0,0,.1)'}">
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
          }
        ]
      },
      shadows: [{
          name: 'Small',
          size: 10,
          smooth: 0
        },
        {
          name: 'Medium',
          size: 20,
          smooth: 5
        },
        {
          name: 'Large',
          size: 30,
          smooth: 10
        }
      ],
      gradients: [{
          name: 'Primary',
          color: '#757de8',
          color2: '#002984'
        },
        {
          name: 'Dark',
          color: '#4f4f4f',
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
