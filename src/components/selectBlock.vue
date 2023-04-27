<template>
    <div>
        <select @change="sel" v-model="colorEyes">
            <option value="лысый" selected>
                лысый
            </option>
            <option value="полосатый">
                полосатый
            </option>
            <option value="взъерошенный">
                взъерошенный
            </option>
        </select>
    </div>
</template>

<script>
export default {
    name: "selectBlock",
    data () {
        return {
            colorEyes: '',
        }
    },
    props: ['select'],
    methods: {
        sel () {
            this.$emit('sel', this.colorEyes)
        }
    }
}
</script>

<style scoped>
select {
    width: 400px;
    height: 50px;
    margin-bottom: 20px;
    font-size: 20px;
}
</style>