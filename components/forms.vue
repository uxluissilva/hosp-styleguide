<template>
<div class="size margin">
  <div class="example">
    <div class="forms-styleguide container column">
    <titleComponent :config="config.title" />

      <div class="forms-block">
        <div class="forms-block__item forms-comp">
          <titleComponent :config="config.subTitle.var" />
          <div class="forms-comp__list-block padding-40">
            <ul class="forms-list">
              <li class="forms-list__item">Form field</li>
              <li class="forms-list__item">Campo pesquisa</li>
              <li class="forms-list__item">Checkboxes</li>
              <li class="forms-list__item">Radio button</li>
              <li class="forms-list__item">Select field</li>
              <li class="forms-list__item">Tabela - Grids</li>
            </ul>
          </div>
        </div>

        <div class="forms-block__item form-field-ex">
          <titleComponent :config="config.subTitle.fields" />

          <div class="container column padding-20">
            <formField :config="config.fields.basic" />
            <formField :config="config.fields.placeholder" />
          </div>

          <div class="container wrap padding-20">
            <selectField :config="config.fields.checkbox" class="margin-right-50" />
            <selectField :config="config.fields.radio" class="margin-right-50" />
            <selectField :config="config.fields.select" />
          </div>

          <div class="container column padding-20">

          </div>
        </div>


      </div>
    </div>

  </div>
</div>
</template>

<script>
import titleComponent from '@/components/titleComponent';
import formField from '@/components/forms/formField';
import selectField from '@/components/forms/selectField';

export default {
  name: 'forms',
  components: {
    titleComponent,
    formField,
    selectField
  },
  data() {
    return {
      config: {
        title: {
          order: 2,
          text: "Formulários"
        },
        subTitle: {
          var: {
            order: 3,
            text: "Lista de componentes"
          },
          fields: {
            order: 3,
            text: "Form field - campo texto"
          },
          search: {
            order: 3,
            text: "Campo de pesquisa"
          },
          selectBoxes: {
            order: 3,
            text: "Campos de seleção - checkbox, radio & select"
          },
          table: {
            order: 3,
            text: "Tabelas - Grids"
          },
          mask: {
            order: 3,
            text: "Máscara para preenchimento"
          },
          validation: {
            order: 3,
            text: "Validação de formulários"
          }
        },
        fields: {
          basic: {
            style: 0,
            label: "Nome completo"
          },
          placeholder: {
            style: 0,
            label: "Celular",
            placeholder: "(44) 9 9999-9999"
          },
          select: {
            style: 0,
            label: "Estado Civil",
            items: [
              "Solteiro(a)",
              "Casado(a)",
              "Divorciado(a)",
              "Viúvo(a)"
            ]
          },
          checkbox: {
            type: 0,
            title: "Checkbox",
            labels: [
              "Option 1",
              "Option 2",
              "Option 3"
            ]
          },
          radio: {
            type: 1,
            title: "Radio",
            labels: [
              "Option 1",
              "Option 2",
              "Option 3"
            ]
          },
          select: {
            type: 2,
            title: "Estado Civil",
            labels: [
              "Solteiro(a)",
              "Casado(a)",
              "Divorciado(a)",
              "Viúvo(a)"
            ]
          }
        }
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.forms-styleguide {
  width: 100%;

  .forms-block {
    .forms-block__item {
      width: 100%;

      .forms-example {

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
