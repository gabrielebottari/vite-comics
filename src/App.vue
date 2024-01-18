<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppMainMenu from './components/AppMainMenu.vue';
import AppFooter from './components/AppFooter.vue';

export default {
    data() {
        return {

        };
    },
    components: {
        AppHeader,
        AppMain,
        AppMainMenu,
        AppFooter,
    },  
    methods: {

    }
}
</script>

<template>

    <AppHeader />

    <AppMain />

    <AppMainMenu />

    <AppFooter />
</template>

<style lang="scss">
@use "assets/scss/main" as *;
@import "assets/scss/partials/reset";
</style>