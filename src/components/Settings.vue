<template>
    <div>
        <Results/>
        <h1 class="header">Настройки</h1>
        <v-divider class="divider"></v-divider>
        <section class="elevation-18 settings">
        <v-container fluid>
        <v-form class="form">
            <v-text-field
                    id="time"
                    class="property"
                    v-model="time"
                    label="Время для решения задач"
            />
            <v-select
                    v-model="level"
                    class="property"
                    label="Уровень сложности"
                    :items="levels"
            />
            <v-checkbox
                v-model="summation"
                :label="'Сложение'"/>
            <v-checkbox
                    v-model="difference"
                    :label="'Разность'"/>
            <v-checkbox
                    v-model="multiplication"
                    :label="'Умножение'"/>
            <v-checkbox
                    v-model="division"
                    :label="'Деление'"/>
            <v-checkbox
                    v-model="exponentiation"
                    :label="'Возведение в степень'"/>
        </v-form>
        </v-container>
    </section>
        <v-btn color="primary" style="position: fixed;
    right: 2%;
    margin-top: 5%;" @click="runPlay"> Играть!</v-btn>
    </div>
</template>

<script>
import Results from "./Results";
export default {
    name: 'Settings',
    components: {Results},
    data: () => {
        return {
            time: 15,
            level: null,
            levels: ['легкий', 'средний', 'сложный'],
            summation: null,
            difference: null,
            multiplication: null,
            division: null,
            exponentiation: null
        }
    },
    props: {

    },
    methods: {
        runPlay() {
            console.log('Игра начинается');
        }
    }
}
</script>


<style>
    .settings{
        margin-left: 2%;
        margin-top: 1%;
        margin-right: 2%;
        width: 96%;
    }

    .property {
        width: 35%;
    }
    .form {
        margin-top: 2%;
    }
    .divider {
        background-color: #282828;
        margin-left: 2%;
        width: 40%;
    }
    .header{
        margin-top: 5%;
        margin-left: 2%;
    }
    /*Работает не так, как ожидалось, если использовать класс, а не стиль*/
    .playit {
        position: fixed;
        right: 2%;
        margin-top: 5%;
    }
</style>
