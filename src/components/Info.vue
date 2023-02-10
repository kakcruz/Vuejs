<template>
    <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <ul>
      <li>JavaScript</li>
      <li>Php</li>
      <li>Python</li>
    </ul>
    <div>
    <button @click="showEmail" >{{textoBotao}}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{email}}</p>
    <p>Para acessar meu portifólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
    <Picture/>
    </div>
</template>

<script>
import Picture from './form/Picture.vue'

export default {
    name: 'Info',
    components: {
      Picture
    },
    data(){
      return{
        esta_trabalhando: false,
        mostrar_email: false,
        email: 'kakcruz@email.com',
        meu_link: 'https://www.google.com/',
        textoBotao: 'Mostrar E-mail'
      }
    },
    methods:{
      showEmail(){
        this.mostrar_email = !this.mostrar_email
        if(!this.mostrar_email){
          this.textoBotao = 'Mostrar E-mail'
        } else {
          this.textoBotao = 'Esconder E-mail'
        }
      }
    }
}
</script>