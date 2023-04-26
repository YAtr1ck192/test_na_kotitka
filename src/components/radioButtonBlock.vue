<template>
    <div>
        <div class="radio-content">
            <label :for="radio.id">
                {{ radio.color }}
            </label>
            <input
                name="radio"
                type="radio"
                :id="radio.id"
                :value="radio.color"
                v-model="colorWool"
                @change="rad"
            >
        </div>
        <img :src="radio.img" alt="color">
    </div>
</template>
<script>
export default {
    name: "radioButtonBlock",
    data () {
        return {
            colorWool: ''
        }
    },
    props: ['radio'],
    methods: {
        rad () {
            this.$emit('rad', this.colorWool)
        }
    }
}
</script>

<style scoped>
h2 {
    text-align: center;
}
img {
    max-width: 300px;
}

input {
    margin-bottom: 20px;
}
</style>