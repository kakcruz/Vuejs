<template>
    <div>
    <p>{{ compEmail}}</p>
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Estou em busca de novas oportunidades</p>
    <p>Utilizo as seguintes tecnologias para back-end:</p>
    <ul>
      <li v-for="(technology, index) in backend_technologies" v-bind:key="index">{{ technology }}</li>
    </ul>
    <p>Utilizo as seguintes tech para front-ed:</p>
    <ul>
    <li v-for="technology in frontend_technologies" :key="technology.id">
      {{ technology.language }}
    </li>
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
    props:{
      email: String
    },
    data(){
      return{
        esta_trabalhando: false,
        mostrar_email: false,
        meu_link: 'https://www.google.com/',
        textoBotao: 'Mostrar E-mail',
        backend_technologies: ['JavaScript' , 'PHP' , 'Python' , 'Java'],
        frontend_technologies: [
          {id: 1, language: 'HTML'},
          {id: 2, language: 'CSS'},
          {id: 3,language: 'Javascript'}
        ]
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