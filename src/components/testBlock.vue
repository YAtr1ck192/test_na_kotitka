<template>
<div id="test">
    <h2>Какой ты сегодня?</h2>
    <div class="container">
        <div class="box">
            <div>
                <div class="checkbox-content">
                    <label for="funny">
                        радостный
                    </label>
                    <input
                            type="checkbox"
                            value="радостный"
                            id="funny"
                            v-model="checkboxResult"
                    >
                </div>
                <img src='/images/funny.jpg' alt="mood">
            </div>
            <div>
                <div class="checkbox-content">
                    <label for="sad">
                        грустный
                    </label>
                    <input
                            type="checkbox"
                            value="грустный"
                            id="sad"
                            v-model="checkboxResult"
                    >
                </div>
                <img src='/images/sad.jpg' alt="mood">
            </div>
            <div>
                <div class="checkbox-content">
                    <label for="sleepy">
                        сонный
                    </label>
                    <input
                            type="checkbox"
                            value="сонный"
                            id="sleepy"
                            v-model="checkboxResult"
                    >
                </div>
                <img src='/images/sleepy.jpg' alt="mood">
            </div>
        </div>
        <p
                v-if="checkboxResult.length !== 0"
        >
            Вы выбрали {{ checkboxResult }}
        </p>
    </div>
    <h2>
        Какой цвет тебе больше подходит?
    </h2>
    <div class="container">
        <div class="box">
            <radioButtonBlock
                    v-for="item in radioItems"
                    :key="item"
                    :radio="item"
                    @rad="radioResult = $event"
            />
        </div>
        <p
                v-if="radioResult !== ''"
        >
            Вы выбрали: {{ radioResult }}
        </p>
    </div>
    <h2>
        Немного поточнее
    </h2>
    <div class="container">
            <selectBlock
                    @sel="selectResult = $event"
            />
        <p
            v-if="selectResult"
        >
            Вы выбрали: {{ selectResult }}
        </p>
    </div>
    <button
            @click="result = !result">
        Посмотреть результат
    </button>
    <p
        v-if="result"
    >
        {{ res }}
    </p>
</div>
</template>

<script>
import selectBlock from "@/components/selectBlock.vue";
import radioButtonBlock from "@/components/radioButtonBlock.vue";
export default {
    name: "testBlock",
    data () {
        return {
            checkboxResult: [],
            radioItems: [
                {
                    color: 'рыжий',
                    img: '/images/orange-wool.jpg',
                    id: 'orange',
                    index: 0
                },
                {
                    color: 'серый',
                    img: '/images/grey-wool.jpg',
                    id: 'grey',
                    index: 1
                },
                {
                    color: 'черный',
                    img: '/images/black-wool.jpg',
                    id: 'black',
                    index: 2
                },
            ],
            radioResult: '',
            selectResult: '',
            result: false
        }
    },
    components: {
        selectBlock,
        radioButtonBlock,
    },
    methods: {

    },
    computed: {
        res: function () {
            return 'Вы ' + this.checkboxResult + ' ' + this.radioResult + ' ' + this.selectResult + ' кот'
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
#test {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}
.box {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 940px;
}
p {
    text-align: center;
    margin-bottom: 20px;
}
button {
    background: #9747fa;
    border: none;
    color: white;
    padding: 10px 20px;
    border-radius: 20px;
    font-size: 20px;
    margin-bottom: 50px;
    cursor: pointer;
}
button:hover {
    background: #6e35b4;
}
</style>