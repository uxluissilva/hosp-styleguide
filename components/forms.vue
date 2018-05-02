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
          <titleComponent :config="config.subTitle.search" />

          <div class="container column padding-20">
            <searchField :config="config.fields.search" class="margin-right-20"/>
          </div>
        </div>

        <div class="forms-block__item form-field-ex">
          <titleComponent :config="config.subTitle.fields" />

          <div class="container wrap padding-20">
            <formField :config="config.fields.basic" class="margin-right-20"/>
            <formField :config="config.fields.placeholder" class="margin-right-20" />
            <formField :config="config.fields.percent" class="margin-right-20" />
            <formField :config="config.fields.email" class="margin-right-20" />
            <formField :config="config.fields.date" class="margin-right-20" />
            <formField :config="config.fields.zipcode" class="margin-right-20" />
            <formField :config="config.fields.cpf" class="margin-right-20" />
            <formField :config="config.fields.rg" class="margin-right-20" />
            <formField :config="config.fields.aera" class="margin-right-20" />
          </div>
        </div>

        <div class="forms-block__item form-field-ex">
          <titleComponent :config="config.subTitle.selectBoxes" />

          <div class="container wrap padding-20">
            <selectField :config="config.fields.checkbox" class="margin-right-50" />
            <selectField :config="config.fields.radio" class="margin-right-50" />
            <selectField :config="config.fields.select" />
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
import searchField from '@/components/forms/searchField';

export default {
  name: 'forms',
  components: {
    titleComponent,
    formField,
    selectField,
    searchField
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
            order: 4,
            text: "Form field - campo texto"
          },
          search: {
            order: 4,
            text: "Campo de pesquisa"
          },
          selectBoxes: {
            order: 4,
            text: "Campos de seleção - checkbox, radio & select"
          },
          table: {
            order: 4,
            text: "Tabelas - Grids"
          },
          mask: {
            order: 4,
            text: "Máscara para preenchimento"
          },
          validation: {
            order: 4,
            text: "Validação de formulários"
          }
        },
        fields: {
          search: {
            style: "search",
            label: "Pesquisar",
            placeholder: "Digite aqui sua pesquisa...",
            button: {
              style: "",
              text: "Pesquisar"
            }
          },
          basic: {
            style: "text",
            label: "Nome completo"
          },
          placeholder: {
            style: "phone",
            label: "Celular",
            placeholder: "(44) 9 9999-9999"
          },
          percent: {
            style: "percent",
            label: "Percentual",
            placeholder: "0,00%"
          },
          email: {
            style: "email",
            label: "E-mail",
            placeholder: "email@email.com"
          },
          date: {
            style: "date",
            label: "Data",
            placeholder: "01/01/2018"
          },
          zipcode: {
            style: "zipcode",
            label: "CEP",
            placeholder: "87050-000"
          },
          cpf: {
            style: "cpf",
            label: "CPF",
            placeholder: "123.456.789-00"
          },
          rg: {
            style: "rg",
            label: "RG",
            placeholder: "12.345.678-9"
          },
          area: {
            style: "textarea",
            label: "Texto",
            placeholder: "Insira seu texto aqui"
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
