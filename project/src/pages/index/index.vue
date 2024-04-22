<template>
    <CustomNav />
    <scroll-view scroll-y>
        <GuluSwiper :list="list"/>
        <CategoryPanel />
        <ServiceCounter /> 
    </scroll-view>
</template>

<script setup lang="ts">
import CustomNav from './components/CustomNav.vue';
import CategoryPanel from './components/CategoryPanel.vue'
import ServiceCounter from './components/ServiceCounter.vue';

const list = [
    {
        id:1,
        imgUrl:'../../static/images/首页轮播1.jpg',
        hrefUrl:'#'
    },
    {
        id:2,
        imgUrl:'../../static/images/首页轮播2.jpeg',
        hrefUrl:'#'
    },
    {
        id:3,
        imgUrl:'../../static/images/首页轮播3.jpeg',
        hrefUrl:'#'
    }
]

</script>

<style scoped>

</style>