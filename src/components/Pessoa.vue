<template>
  <div>
    <h2>Está é a descrição da pessoa: {{ nome }}</h2>
    <Info :email="email"/>
    <Form/>
  </div>
</template>

<script>
import Info from './Info.vue'
import Form from './form/Form.vue'
export default {
  name: "Pessoa",
  components: {
    Info,
    Form
  },
  data() {
    return {
      nome: "Kakcruz",
      email: "KAKCRUZVUE@VUE.COM.BR"
    };
  },
};
</script>
