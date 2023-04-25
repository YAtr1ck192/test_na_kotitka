<template>
    <div>
        <h2>Какой ты сегодня?</h2>
        <div class="container">
            <div class="checkbox">
                <div class="checkbox-content">
                    <label for="funny">
                        Радостный
                    </label>
                    <input type="checkbox" id="funny" name="mood">
                </div>
                <img src="/images/funny.jpg" alt="mood">
            </div>

            <div class="checkbox">
                <div class="checkbox-content">
                    <label for="sad">
                        Грустный
                    </label>
                    <input type="checkbox" id="sad" name="mood">
                </div>
                <img src="/images/sad.jpg" alt="mood">
            </div>

            <div class="checkbox">
                <div class="checkbox-content">
                    <label for="sleepy">
                        Сонный
                    </label>
                    <input type="checkbox" id="sleepy" name="mood">
                </div>
                <img src="/images/sleepy.jpg" alt="mood">
            </div>
        </div>
    </div>
</template>


<script>
export default {
    name: "checkboxBlock",
    data () {
        return {
            mes: 'ky'
        }
    }
}
</script>

<style scoped>
img {
    width: 300px;
    height: 150px;
}
.checkbox {
    display: flex;
    align-items: flex-start;
    justify-content: center;
    flex-direction: column;
}
.checkbox:nth-child(2) {
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