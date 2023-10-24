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

import magazineImg from './magazine1.png'

const items = ref([
    { title: 'HTML', src: htmlIcon, alt: 'Ícone do HTML5' },
    { title: 'CSS', src: cssIcon, alt: 'Ícone do CSS3' },
    { title: 'JavaScript', src: javascriptIcon, alt: 'Ícone do JavaScript' },
    { title: 'SASS', src: sassIcon, alt: 'Ícone do SASS' },
    { title: 'Vue', src: vueIcon, alt: 'Ícone do Vue' },
    { title: 'Vuetify', src: vuetifyIcon, alt: 'Ícone do Vuetify' },
    { title: 'Vuex', src: vuexIcon, alt: 'Ícone do Vuex' },
    { title: 'PHP', src: phpIcon, alt: 'Ícone do PHP' },
    { title: 'Laravel', src: laravelIcon, alt: 'Ícone do Laravel' },
    { title: 'Mysql', src: mysqlIcon, alt: 'Ícone do Mysql' },
])
</script>

<template>
    <div class="project">
        <div class="project__content">
            <span class="project__label">Projeto</span>
            <h4 class="project__title">Magazine Brindes</h4>
            <p class="project__text">Magazine Brindes é uma empresa que atua no ramo de venda de produtos personalizados em larga escala. O sistema desenvolvido se trata de um ERP para gerir pessoas, etoque e financeiro.
            Além disso, o projeto conta com uma seção para gestão do site, onde o usuário pode mudar os banners, inserir novos parceiros, manipular produtos em destaque, etc.</p>
        </div>
        <div class="project__image">
            <figure>
                <img :src="magazineImg.src" style="width: 100%" alt="Imagem do projeto Magazine Brindes">
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