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
                     @click="check"
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
            res: [],
            active: false,
            noActive: ''
        }
    },
    props: ['checkbox'],
    methods: {
        check () {
            if (this.active === false) {
                this.active = !this.active
                this.$emit('check', this.res.toString())
            } else {
                this.$emit('check', this.noActive.toString())
                this.active = !this.active
            }

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