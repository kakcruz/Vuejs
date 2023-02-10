<template>
  <div>
  <img :src="avatar" :alt="descricao"> <!--Os dois pontos( : ) atrás de src, é uma sintaxe resumida de v-bind -->
  </div>
</template>

<script>

export default {
    name: 'Picture',
    data(){
        return{
            avatar: "/img/avatar.png",
            descricao: "Kakcruz"
        }
    }
}
</script>