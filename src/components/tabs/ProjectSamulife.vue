<script setup>
import { ref } from 'vue'
import htmlIcon from '/src/icons/html.vue'
import cssIcon from '/src/icons/css.vue'
import javascriptIcon from '/src/icons/javascript.vue'
import sassIcon from '/src/icons/sass.vue'
import vueIcon from '/src/icons/vueicon.vue'
import vuetifyIcon from '/src/icons/vuetify.vue'
import vuexIcon from '/src/icons/vuex.vue'
import phpIcon from '/src/icons/php.vue'
import laravelIcon from '/src/icons/laravel.vue'
import mysqlIcon from '/src/icons/mysql.vue'

import samulifeImg from './samulife1.png'

const items = ref([
    { title: 'HTML', src: htmlIcon, alt: 'Ícone do HTML5' },
    { title: 'CSS', src: cssIcon, alt: 'Ícone do CSS3' },
    { title: 'JavaScript', src: javascriptIcon, alt: 'Ícone do JavaScript' },
    { title: 'PHP', src: phpIcon, alt: 'Ícone do PHP' },
    { title: 'Vue', src: vueIcon, alt: 'Ícone do Vue' },
    { title: 'Laravel', src: laravelIcon, alt: 'Ícone do Laravel' },
    { title: 'SASS', src: sassIcon, alt: 'Ícone do SASS' },
    { title: 'Vuetify', src: vuetifyIcon, alt: 'Ícone do Vuetify' },
    { title: 'Vuex', src: vuexIcon, alt: 'Ícone do Vuex' },
    { title: 'Mysql', src: mysqlIcon, alt: 'Ícone do Mysql' },
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
                <img :src="samulifeImg.src" width="100%" alt="Imagem do projeto Samulife">
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