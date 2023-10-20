<script setup>
import { ref } from 'vue'

const items = ref([
    { title: 'HTML', src: '/src/assets/svg-icons/html.svg', alt: 'Ícone do HTML5' },
    { title: 'CSS', src: '/src/assets/svg-icons/css.svg', alt: 'Ícone do CSS3' },
    { title: 'JavaScript', src: '/src/assets/svg-icons/javascript.svg', alt: 'Ícone do JavaScript' },
    { title: 'SASS', src: '/src/assets/svg-icons/sass.svg', alt: 'Ícone do SASS' },
    { title: 'Vue', src: '/src/assets/svg-icons/vue.svg', alt: 'Ícone do Vue' },
    { title: 'Vuetify', src: '/src/assets/svg-icons/vuetify.svg', alt: 'Ícone do Vuetify' },
    { title: 'Vuex', src: '/src/assets/svg-icons/vuex.svg', alt: 'Ícone do Vuex' },
    { title: 'PHP', src: '/src/assets/svg-icons/php.svg', alt: 'Ícone do PHP' },
    { title: 'Laravel', src: '/src/assets/svg-icons/laravel.svg', alt: 'Ícone do Laravel' },
    { title: 'Mysql', src: '/src/assets/svg-icons/mysql.svg', alt: 'Ícone do Mysql' },
])
</script>

<template>
    <div class="project">
        <div class="project__content">
            <span class="project__label">Projeto</span>
            <h4 class="project__title">Samulife</h4>
            <p class="project__text">Samulife é o sistema criado para registros de atendiomento na emergência do estado da Bahia.
            Com este sistema é possível cadastrar novas fichas com um esquema de passo a passo, onde o usuário cadastra partes de uma ficha baseado em sua permissão.O sistema conta com uma seção para gerenciar usuários e suas permissões, variando entre usuários comum, enfermeiros e médicos.</p>
        </div>
        <div class="project__image">
            <figure>
                <img style="color: red" src="/src/assets/projects/samulife1.png" width="100%" alt="Imagem do projeto Síntese">
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
                    <img :src="item.src" :alt="item.alt">
                    <span>{{ item.title }}</span>
                </li>
            </ul>
        </div>
    </div>
</template>