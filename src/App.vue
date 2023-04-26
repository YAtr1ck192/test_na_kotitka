<template>
    <div id="app">
        <h1>Кто ты из котиков ଲ(ⓛ ω ⓛ)ଲ</h1>
        <testBlock />
    </div>
</template>

<script>

import testBlock from "@/components/testBlock.vue";

export default {
    name: 'App',
    components: {
        testBlock
    }
}
</script>

<style>
    #app {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }
</style>
