<template>
  <div>
  <img :src="avatar" :alt="descricao"> <!--Os dois pontos( : ) atrás de src, é uma sintaxe resumida de v-bind -->
  <MudarImagem @mudar-imagem="trocarImagem" /> <!--O mudar-imagem é o emit que ativa o metodod trocar imagem-->
  </div>
</template>

<script>
    import MudarImagem from './MudarImagem.vue'
export default {

    name: 'Picture',
    data(){
        return{
            avatar: "/img/avatar.png",
            descricao: "Kakcruz"
        }
    },
    components: {
        MudarImagem
    },
    methods:{
        trocarImagem(){
            this.avatar = "/img/avatar2.png"
            
        }

    }
}
</script>