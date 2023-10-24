<script setup>
import { ref } from 'vue'
import htmlIcon from '/src/icons/html.vue'
import cssIcon from '/src/icons/css.vue'
import javascriptIcon from '/src/icons/javascript.vue'
import sassIcon from '/src/icons/sass.vue'
import vueIcon from '/src/icons/vueicon.vue'
import vuexIcon from '/src/icons/vuex.vue'
import quasarIcon from '/src/icons/quasar.vue'
import nodeIcon from '/src/icons/node.vue'
import mongoIcon from '/src/icons/mongo.vue'
import sinteseImg from './sintese1.png'

const items = ref([
    { title: 'HTML', src: htmlIcon, alt: 'Ícone do HTML5' },
    { title: 'CSS', src: cssIcon, alt: 'Ícone do CSS3' },
    { title: 'JavaScript', src: javascriptIcon, alt: 'Ícone do JavaScript' },
    { title: 'SASS', src: sassIcon, alt: 'Ícone do SASS' },
    { title: 'Vue', src: vueIcon, alt: 'Ícone do Vue' },
    { title: 'Quasar Framework', src: quasarIcon, alt: 'Ícone do Quasar Framework' },
    { title: 'Vuex', src: vuexIcon, alt: 'Ícone do Vuex' },
    { title: 'Node', src: nodeIcon, alt: 'Ícone do Node' },
    { title: 'Mongo DB', src: mongoIcon, alt: 'Ícone do Mongo DB' },
])
</script>

<template>
    <div class="project">
        <div class="project__content">
            <span class="project__label">Projeto</span>
            <h4 class="project__title">Síntese</h4>
            <p class="project__text">Síntese é uma escola de dança aqui da minha cidade, que inclusive eu sou aluno 😅.
            Este é um sistema ainda em desenvolvimento, é meu projeto mais recente.
            Se trata de uma aplicação capaz de gerir alunos e professores bem como as entradas e saídas do financeiro da escola.Com este sistema é possível inserir novos alunos e professores, criar novas turmas e modalidades, cadastrar novas receitas e novas despesas.</p>
        </div>
        <div class="project__image">
            <figure>
                <img :src="sinteseImg.src" style="width: 100%" alt="Imagem do projeto Síntese">
            </figure>
        </div>
        <div class="project__footer">
            <h4 class="project__title">Tecnologias Utilizadas</h4>
            <ul class="project__footer__list">
                <li
                    class="project__chips"
                    v-for="(item, idx) in items"
                    :key="idx"
                >
                    <component :is="item.src" />
                    <span>{{ item.title }}</span>
                </li>
            </ul>
        </div>
    </div>
</template>