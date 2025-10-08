<script setup>
import About from '../customelements/About.vue';
import Header from '../customelements/Header.vue';
import Project from '../customelements/Project.vue';

const emit = defineEmits(["AddComponent"])

const AddComponent = (comp) => {
    emit("AddComponent", comp);
}

const elementList = [
    {
        title:"Header",
        elements:[
            Header
        ]
    },
    {
        title:"Content",
        elements:[
            About,
            Project
        ]
    }
]

</script>
<template>
    <template v-for="(subsections,index) in elementList" :key="index">
        <h1>{{ subsections.title }}</h1>
        <template v-for="(element,index) in subsections.elements" :key="index">
            <component :is="element" @AddComponent="AddComponent"></component>
        </template>
    </template>
</template>