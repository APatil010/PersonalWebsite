<script setup>
import NavigationBar from "./components/NavigationBar.vue";
</script>

<template>
    <NavigationBar />
    <router-view />
</template>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto+Mono:300,400,500&display=swap');

body {
    margin: 0 20%;
    font-family: 'Roboto Mono', monospace;
}

a, a:hover, a:visited, a:active, a:link {
    text-decoration: none;
    color: black;
}

.mono-light {
    font-weight: 300;
}
.font-40 {
    font-size: 40px;
}
.font-28 {
    font-size: 28px;
}
.font-20 {
    font-size: 20px;
}
.font-18 {
    font-size: 18px;
}
.font-16 {
    font-size: 16px;
}
</style>
