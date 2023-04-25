<template>
    <div>
        <h2>
            Какой твой любимый цвет (только 1)
        </h2>
        <div class="container">
            <div class="radio">
                <div class="radio-content">
                    <label for="orange">
                        orange
                    </label>
                    <input type="radio" id="orange" name="color">
                </div>
                <img src="/images/orange-wool.jpg" alt="color">
            </div>

            <div class="radio-box">
                <div class="radio-content">
                    <label for="grey">
                        grey
                    </label>
                    <input type="radio" id="grey" name="color">
                </div>
                <img src="/images/grey-wool.jpg" alt="color">
            </div>
            <div class="radio-box">
                <div class="radio-content">
                    <input type="radio" id="black" name="color">
                    <label for="black">
                        black
                    </label>
                </div>
                <img src="/images/black-wool.jpg" alt="color">
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: "radioButtonBlock",
    data () {
        return {
            mes: 'ky'
        }
    }
}
</script>

<style scoped>
img {
    max-width: 300px;
}
.radio-box {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    flex-direction: column;
}
.radio-box:nth-child(2) {
    margin: 0 20px;
}
.container {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto;
    max-width: 80%;
}
input {
    margin-bottom: 20px;
}
</style>