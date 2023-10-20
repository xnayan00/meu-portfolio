<script setup>
import { ref } from 'vue'
import ProjectSintese from './ProjectSintese.vue'
import ProjectMagazine from './ProjectMagazine.vue'
import ProjectSamulife from './ProjectSamulife.vue'

var currentTab = ref(1)
const tabs = ref([
    { id: 1, title: 'Síntese' },
    { id: 2, title: 'Magazine' },
    { id: 3, title: 'Samulife' },
])

const projects = ref([ProjectSintese, ProjectMagazine, ProjectSamulife])

const toggleTab = (value) => {
    currentTab.value = value
}

</script>

<template>
    <article class="container">
        <div class="tabs">
            <div
                v-for="tab in tabs"
                :key="tab.id"
                @click="toggleTab(tab.id)"
                class="tabs__item"
                :class="{'tabs__item--active': tab.id === currentTab}"
                role="button"
            >
                {{ tab.title }}
            </div>
        </div>
        <div class="tabs__content">
            <component :is="projects[currentTab - 1]" />
        </div>
    </article>
</template>