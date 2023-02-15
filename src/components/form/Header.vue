<template>
  <div>
    <ul>
      <li><a href="">Home</a></li>
      <li><a href="">Projetos</a></li>
      <li><a href="">Contato</a></li>
      <li><a v-if="esta_logado">Meu Perfil</a></li>
    </ul>
  </div>
</template>

<script>
export default {
    name: 'Header',
    props: [
      "esta_logado"
    ]
};
</script>

<style scoped>
    div{
        background: gray ;
    }
    ul{
       list-style: none; 
       display: flex;
    }

    li{
        margin-right: 10px;

    }
    a{
        color: white;
        text-decoration: none;
        transition: .5s;
    }
    a:hover{
        color: blueviolet;
    }

</style>
