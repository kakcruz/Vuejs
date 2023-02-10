<template>
  <div>
  <h2>Meu formulario:</h2>
    <form action="">
      <div>
        <inputText />
      </div>
      <div>
        <inputText />
      </div>
      <div>
        <Submit />
      </div>
    </form>
  </div>
</template>

<script>
import InputText from "./InputText.vue";
import Submit from "./Submit.vue";

export default {
  name: "Form",
  components: {
    InputText,
    Submit,
  },
};
</script>
