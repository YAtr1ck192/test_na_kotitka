<template>
    <div>
         <div class="checkbox-content">
            <label :for="checkbox.id">
                {{ checkbox.mood }}
            </label>
             <input
                     type="checkbox"
                     :value="checkbox.mood"
                     :id="checkbox.id"
                     v-model="res"
                     @change="check"
             >
         </div>
         <img :src="checkbox.img" alt="mood">
    </div>
</template>


<script>
export default {
    name: "checkboxBlock",
    data () {
        return {
            res: []
        }
    },
    props: ['checkbox'],
    methods: {
        check () {
            this.$emit('check', this.res.toString())
        }
    }
}
</script>

<style scoped>
h2 {
    text-align: center;
}
img {
    width: 300px;
    height: 150px;
}
input {
    margin-bottom: 20px;
}
</style>