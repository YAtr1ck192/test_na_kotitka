<template>
    <div id="app">
        <h1>Кто ты из котиков ଲ(ⓛ ω ⓛ)ଲ</h1>
        <checkboxBlock />
        <radioButtonBlock />
        <selectBlock />

    </div>
</template>

<script>

import checkboxBlock from "@/components/checkboxBlock.vue";
import selectBlock from "@/components/selectBlock.vue";
import radioButtonBlock from "@/components/radioButtonBlock.vue";

export default {
    name: 'App',
    components: {
        checkboxBlock,
        selectBlock,
        radioButtonBlock
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
